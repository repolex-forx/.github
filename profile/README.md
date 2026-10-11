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
| [certifi/cert-tools](https://github.com/repolex-forx/certifi--cert-tools) | `94ff3b87f5` | 2026-10-11 |
| [certifi/node-certifi](https://github.com/repolex-forx/certifi--node-certifi) | `868e391030` | 2026-10-11 |
| [certifi/certifi-prompt](https://github.com/repolex-forx/certifi--certifi-prompt) | `c5ccd2e616` | 2026-10-11 |
| [certifi/extract-nss-root-certs](https://github.com/repolex-forx/certifi--extract-nss-root-certs) | `96377fcbd1` | 2026-10-11 |
| [dateutil/deadsnakes-action](https://github.com/repolex-forx/dateutil--deadsnakes-action) | `dafca658ce` | 2026-10-11 |
| [certifi/certifi.io](https://github.com/repolex-forx/certifi--certifi.io) | `545cdb27ae` | 2026-10-11 |
| [chardet/chardet.github.io](https://github.com/repolex-forx/chardet--chardet.github.io) | `489dd0b0b5` | 2026-10-11 |
| [celery/celerytest](https://github.com/repolex-forx/celery--celerytest) | `39c7175824` | 2026-10-11 |
| [celery/umbrella](https://github.com/repolex-forx/celery--umbrella) | `02b5ca0a4a` | 2026-10-11 |
| [celery/.github](https://github.com/repolex-forx/celery--.github) | `19fb6c9041` | 2026-10-11 |
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
