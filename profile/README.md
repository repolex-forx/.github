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
| [encode/httpx](https://github.com/repolex-forx/encode--httpx) | 0.12.1 | 2026-09-24 |
| [Python-Markdown/markdown](https://github.com/repolex-forx/Python-Markdown--markdown) | 2.0-Final | 2026-09-24 |
| [Kludex/uvicorn](https://github.com/repolex-forx/Kludex--uvicorn) | 0.14.0 | 2026-09-24 |
| [giampaolo/psutil](https://github.com/repolex-forx/giampaolo--psutil) | v5.6.3 | 2026-09-24 |
| [python-pillow/Pillow](https://github.com/repolex-forx/python-pillow--Pillow) | 10.1.0 | 2026-09-24 |
| [urllib3/urllib3](https://github.com/repolex-forx/urllib3--urllib3) | 1.25.6 | 2026-09-24 |
| [jd/tenacity](https://github.com/repolex-forx/jd--tenacity) | 3.1.0 | 2026-09-24 |
| [samuelcolvin/watchfiles](https://github.com/repolex-forx/samuelcolvin--watchfiles) | v1.1.1 | 2026-09-24 |
| [MagicStack/httptools](https://github.com/repolex-forx/MagicStack--httptools) | v0.7.1 | 2026-09-24 |
| [repolex-ai/forx](https://github.com/repolex-forx/repolex-ai--forx) | `3fc54e02b9` | 2026-09-24 |
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
