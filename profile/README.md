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
| [oven-sh/bun-development-docker-image](https://github.com/repolex-forx/oven-sh--bun-development-docker-image) | `88381bd1b6` | 2026-10-10 |
| [tiangolo/repo-redirect](https://github.com/repolex-forx/tiangolo--repo-redirect) | `1e4e8677a6` | 2026-10-10 |
| [oven-sh/awesome-bun](https://github.com/repolex-forx/oven-sh--awesome-bun) | `9b6277f02b` | 2026-10-10 |
| [oven-sh/security-scanner-template](https://github.com/repolex-forx/oven-sh--security-scanner-template) | `a18eb0889a` | 2026-10-10 |
| [oven-sh/style-guide](https://github.com/repolex-forx/oven-sh--style-guide) | `26252c373d` | 2026-10-10 |
| [oven-sh/bun-releases-for-updater](https://github.com/repolex-forx/oven-sh--bun-releases-for-updater) | bun-v1.4.3 | 2026-10-10 |
| [tiangolo/uwsgi-nginx-flask-docker](https://github.com/repolex-forx/tiangolo--uwsgi-nginx-flask-docker) | `0547cf8ecb` | 2026-10-10 |
| [tiangolo/blog-posts](https://github.com/repolex-forx/tiangolo--blog-posts) | `a4dc3df44d` | 2026-10-10 |
| [tiangolo/nginx-rtmp-docker](https://github.com/repolex-forx/tiangolo--nginx-rtmp-docker) | `ff589ceb62` | 2026-10-10 |
| [tiangolo/uwsgi-nginx-docker](https://github.com/repolex-forx/tiangolo--uwsgi-nginx-docker) | `2a3330ace1` | 2026-10-10 |
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
