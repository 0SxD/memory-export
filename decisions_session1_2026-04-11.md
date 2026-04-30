---
name: Session 1 Decisions — 0sXai Naming + Tooling + Memory Protocol
description: Key decisions from Sage in Session 1 — project naming, Obsidian tooling, memory deprecation, file output protocol
type: project
originSessionId: 2ccbe833-32ed-43c5-b42e-b61ec119eded
---
## Decisions — 2026-04-11, Session 1

### 1. Project Naming: 0sXai
- Official OS repo will be called `0sXai` for code and PM purposes
- Multiple names acceptable during build phase — final name decided at end of build
- SandBoxSetup remains the sandbox directory
- Future: C:\Users\Austin.DESKTOP-8AMMKQP\Downloads\SandBoxSetup → eventually 0sXai repo

**Why:** Need a code-friendly name for the repo while keeping creative freedom for branding.
**How to apply:** Use `0sXai` in all code/PM references. Accept multiple names in conversation/design.

### 2. Obsidian Tooling: Open-Source, Audit-Worthy
- Sage confirmed: use a new open-source, audit-worthy Obsidian tool or similar
- Need to research and confirm specific tool
- Must be open-source (auditable codebase)
- Candidates to research: Obsidian (plugins OSS, app closed), Foam, Logseq, Dendron, SilverBullet

**Why:** Wiki/knowledge base needs to be trustworthy, auditable, and compatible with wikilink/markdown format.
**How to apply:** Research top candidates, recommend one, await Sage confirmation before installing.

### 3. Memory Deprecation Tracking
- Indicate when memory entries deprecate
- Sessions become long — need zero context loss
- Researching enhanced memory compression
- Use post-quantum master model references where applicable

**Why:** Long sessions cause context drift. Memory entries rot if not timestamped and freshness-tracked.
**How to apply:** Add deprecation indicators to memory entries. Flag stale entries proactively.

### 4. File Output Protocol (for denied Write agents)
- Opus writes output files directly, acting on behalf of each Sonnet agent
- Reprocess memories while writing to ensure full absorption
- This is the pattern when sub-agents get Write denied

**Why:** Sub-agents get Write denied in sandbox dir. Opus is allowed to write .md files.
**How to apply:** Read agent summaries, read source files for verification, write comprehensive output files.
