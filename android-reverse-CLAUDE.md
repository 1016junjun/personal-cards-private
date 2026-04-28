# CLAUDE.md

Android Reverse Engineering & API Extraction skill for Claude Code. Decompiles APK/XAPK/JAR/AAR and extracts HTTP APIs.

## What it does

| Capability | Description |
|------------|-------------|
| **Decompile** | APK, XAPK, JAR, AAR via jadx and Fernflower/Vineflower |
| **Extract APIs** | Retrofit endpoints, OkHttp calls, hardcoded URLs, auth headers/tokens |
| **Trace call flows** | Activities/Fragments → ViewModels → repositories → HTTP calls |
| **Analyze structure** | Manifest, packages, architecture patterns |
| **Handle obfuscation** | ProGuard/R8 output navigation |

## Requirements

- Java JDK 17+
- jadx (CLI) — required
- Vineflower/Fernflower — optional, recommended for complex Java

## Tool Selection

**Gather info** → use `ctx_batch_execute` for parallel commands.  
**Analyze code** → use `ctx_execute` (JavaScript) instead of reading raw files.  
**Web lookup** → use `ctx_fetch_and_index` then `ctx_search`.  
**Navigation/small cmds** → Bash (`ls`, `cd`, `git`, etc.).

## Activation phrases

- "Decompile this APK"
- "Reverse engineer this Android app"
- "Extract API endpoints from this app"
- "Follow the call flow from LoginActivity"
- "Analyze this AAR library"

## Rules

- DO NOT use Read for analysis — use `ctx_execute` with JavaScript.
- DO NOT dump raw decompiled output into context — summarize and extract.
- Bash only for git, mkdir, navigation, short status commands.
- Write output artifacts to FILES, return file path + 1-line description.

## Output

Technical, terse, exact. No fluff. Code unchanged. Fragments OK.
