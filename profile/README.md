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
| [NousResearch/hermes-plugin-honcho](https://github.com/repolex-forx/NousResearch--hermes-plugin-honcho) | main | 2026-09-29 |
| [NousResearch/hermes-plugin-supermemory](https://github.com/repolex-forx/NousResearch--hermes-plugin-supermemory) | main | 2026-09-29 |
| [NousResearch/hermes-plugin-blender](https://github.com/repolex-forx/NousResearch--hermes-plugin-blender) | main | 2026-09-29 |
| [NousResearch/hermes-plugin-claude-subscription-directsdk](https://github.com/repolex-forx/NousResearch--hermes-plugin-claude-subscription-directsdk) | main | 2026-09-29 |
| [cspotcode/outdent](https://github.com/repolex-forx/cspotcode--outdent) | v0.8.0 | 2026-09-29 |
| [eemeli/yaml](https://github.com/repolex-forx/eemeli--yaml) | v3.0.0-0 | 2026-09-28 |
| [dryoma/postcss-media-query-parser](https://github.com/repolex-forx/dryoma--postcss-media-query-parser) | v0.2.0 | 2026-09-28 |
| [chalk/strip-ansi](https://github.com/repolex-forx/chalk--strip-ansi) | v7.2.0 | 2026-09-28 |
| [pygments/pygments](https://github.com/repolex-forx/pygments--pygments) | 1.5 | 2026-09-28 |
| [alexeyraspopov/picocolors](https://github.com/repolex-forx/alexeyraspopov--picocolors) | v1.1.1 | 2026-09-28 |
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
