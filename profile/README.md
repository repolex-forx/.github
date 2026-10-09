# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [rlex](https://github.com/repolex-ai/rlex), the query tool for repolex knowledge graphs:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Download a parsed repo:

```bash
rlex download repolex-ai/rlex
```

**rlex is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of rlex"
"Hermes, can you use the rlex tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [NousResearch/TextArena](https://github.com/repolex-forx/NousResearch--TextArena) | `2f20590f09` | 2026-10-09 |
| [NousResearch/huskyholdem-bench](https://github.com/repolex-forx/NousResearch--huskyholdem-bench) | `eb149674a4` | 2026-10-09 |
| [NousResearch/local_generative_agents](https://github.com/repolex-forx/NousResearch--local_generative_agents) | `d66508143a` | 2026-10-09 |
| [NousResearch/longform-writing-bench](https://github.com/repolex-forx/NousResearch--longform-writing-bench) | `d1c625505b` | 2026-10-09 |
| [NousResearch/eqbench3](https://github.com/repolex-forx/NousResearch--eqbench3) | `3c21bcc514` | 2026-10-09 |
| [NousResearch/llm-chain](https://github.com/repolex-forx/NousResearch--llm-chain) | `d1c2abfece` | 2026-10-09 |
| [NousResearch/Obsidian](https://github.com/repolex-forx/NousResearch--Obsidian) | `06124f2a8f` | 2026-10-09 |
| [NousResearch/StripedHyenaTrainer](https://github.com/repolex-forx/NousResearch--StripedHyenaTrainer) | `288a526b8e` | 2026-10-09 |
| [NousResearch/nanotron](https://github.com/repolex-forx/NousResearch--nanotron) | `2cde8f6351` | 2026-10-09 |
| [NousResearch/curve25519-dalek](https://github.com/repolex-forx/NousResearch--curve25519-dalek) | `0964f800ab` | 2026-10-09 |
<!-- END AUTO-UPDATED -->

> Browse the full catalog at **[forx-index](https://github.com/repolex-forx/forx-index)**

## What's in each repo?

| Directory | Contents |
|-----------|----------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA |
| `aggregate/ast/` | Combined AST graph per commit — the full codebase structure |
| `aggregate/lsp/` | LSP enrichment: resolved symbols, definitions, references, types |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit |
| `dep/` | Resolved dependency graph with links to other parsed repos |
| `commit/` | Git commit metadata |
| `branch/` `tag/` | Branch and tag metadata |
| `filetree/` | File tree snapshots per commit |

All data is gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), loadable into any triplestore.

---

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [rlex](https://github.com/repolex-ai/rlex)*
