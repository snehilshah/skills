---
name: go-proverbs
description: Go code editing guidance based on selected Go proverbs and user style rules. 
disable-model-invocation: true
---

# Go Proverbs

## Core Rules

- Keep interfaces tiny. Prefer consumer-owned interfaces. Big interface = weak abstraction
- Make zero value useful when designing structs/APIs. Like returning empty slice instead of nil.
- Avoid `interface{}` / `any` unless boundary is truly untyped. Prefer concrete types, small interfaces, or generics
- Copy tiny stable helper instead of adding dependency. Do not add deps for trivial glue. Add dependency only when it pays for itself
- Clear beats clever. Prefer boring code another Go dev can debug fast. 
- Do not create one-line helpers that only return a value, call another function, or perform another basic operation. Inline such operations which avoid adding extra congnitive load.
- Avoid reflection except for framework/library/boundary code where typed code is worse
- Do not merely check errors. Add useful context, logs, handle fallback, or keep caller able to decide
- Design architecture first, then name components so code explains shape. Docs fill details
- Write docs for package/API users, not to narrate obvious implementation
- Do not `panic` for expected failures. Use `panic` only for impossible programmer errors or unrecoverable state

## User Style Rules

- Prefer a named local before return when it improves scan/debug/error handling:

```go
status := buildStatus(report, now)
return status, nil
```

- Direct return is fine for obvious calls:

```go
return strings.TrimSpace(name)
```

- Optimize for readable control flow over fewer lines.

## While Generating Code

1. Read relevant code before writing
2. Preserve behavior and public contracts while generating changes
3. Generate changes only in files already being edited, reviewed, or explicitly requested in current context
4. Apply only relevant proverbs during code generation. Do not do repo-wide cleanup
5. Run `gofmt` after writing
