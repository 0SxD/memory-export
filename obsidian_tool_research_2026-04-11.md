---
name: Obsidian Tool Research — Zettlr Recommended
description: Research results for open-source audit-worthy wiki/knowledge base tool. Zettlr (primary) and Logseq (secondary) recommended. Obsidian disqualified (closed source).
type: project
originSessionId: 2ccbe833-32ed-43c5-b42e-b61ec119eded
---
## Research Date: 2026-04-11 | Agent: Sonnet (obsidian-tool-research)
## Status: Research complete, verified via live GitHub/web searches

### Recommendation: Zettlr (Primary)
- **License:** GPL v3 (fully auditable)
- **Stars:** 12,800 | **Last release:** v4.3.1, April 5, 2026
- **Features:** wikilinks, YAML frontmatter, built-in D3 graph view, folder-based, Windows native
- **No cloud dependency.** Plain markdown files on disk.
- **Risk:** Graph is visualization-only (not interactive navigation). Thin plugin ecosystem.

### Alternative: Logseq (Secondary, with caveats)
- **License:** AGPL-3.0 | **Stars:** 42,000 | **Last commit:** April 10, 2026
- **Risk:** DB version pivot (markdown → SQLite), CLA controversy, outliner-first UX
- **Use if:** graph traversal/navigation is a core daily workflow

### Disqualified
- **Obsidian** — closed source, fails auditability requirement
- **Dendron** — development ceased late 2023
- **AFFiNE, SiYuan** — not plain-markdown-first (proprietary block databases)

### Conditional
- **Foam** — MIT, but stale (last commit June 2025)
- **SilverBullet** — MIT, active, but graph view is community plug only, browser-based UX

**Why:** Sage confirmed: must be open-source and audit-worthy. Zettlr hits all 7 requirements with no major caveats.
**How to apply:** Await Sage confirmation, then install Zettlr v4.3.1 for wiki visualization + graph view.
