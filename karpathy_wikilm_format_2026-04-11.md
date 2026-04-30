---
name: Karpathy WikiLM / Obsidian Format Specification
description: Target format for corpus organization — 3-layer structure with 95% token reduction, sourced from NotebookLM 8659a880
type: reference
---

## Source
NotebookLM notebook 8659a880-3dc9-4b57-beed-3aa5d0092022, session 8662327a, queried 2026-04-11.
Based on Andrej Karpathy's LLM Wiki (WikiLM) pattern with Obsidian as visual frontend.

## Three-Layer Structure

### Layer 1: raw/
- Curated, immutable source documents (PDFs, clips, notes)
- LLM reads as ground truth but NEVER modifies
- Already populated (~24GB in SandBoxSetup/raw/)

### Layer 2: wiki/
- Active knowledge base managed by LLM
- Markdown pages in subfolders: `concepts/`, `entities/`, `sources/`, `comparisons/`
- LLM writes, updates, cross-references
- Currently EMPTY (SandBoxSetup/wiki/) — target for build-out

### Layer 3: Schema (CLAUDE.md / AGENTS.md)
- Naming conventions, page templates, operational workflows
- Transforms generic LLM into disciplined project-specific knowledge worker

## Key Components

### index.md
- Central catalog in wiki/
- Maps all articles by category with links, one-line summaries, metadata
- LLM reads this FIRST to navigate the wiki

### log.md
- Append-only chronological audit log
- Records every operation (ingests, queries, contradiction flags)

### YAML Frontmatter (every note)
```yaml
---
title: [name]
type: [concept|entity|source|comparison]
source: [origin file or URL]
tags: [list]
summary: [single-line summary]
---
```

### [[wikilinks]]
- Obsidian-style links creating semantic knowledge graph
- Visualizable in Obsidian Graph View
- Connects entities and concepts across the wiki

## Token Optimization

- **95% reduction** vs naive document loading
- LLM reads concise index.md → loads only needed files
- Bypasses traditional RAG — knowledge "compiled" at ingestion
- **Context-Augmented Generation (CAG):** with 1M context window, entire markdown corpus loadable
- **Automated Linting:** periodic scans to connect orphans, update stale claims, flag contradictions

## Wiki Organization by Project Stages

### sageXai stages
- OS architecture, biomimicry brain, Trinity, memory, agents, boot sequence, PQC protocol

### FxD stages
- blockchain, repos, BTC, cryptography, smart contracts, xD Vampire Bridge, DAD system

### Each stage includes
- Organized content from raw/
- Outstanding questions that need answering before use
- Cross-references to other stages via [[wikilinks]]
