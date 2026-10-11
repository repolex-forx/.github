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
| [psf/fides-deploy](https://github.com/repolex-forx/psf--fides-deploy) | `6fcea6d243` | 2026-10-11 |
| [psf/gh-migration](https://github.com/repolex-forx/psf--gh-migration) | `96a350c3dd` | 2026-10-11 |
| [psf/community-code-of-conduct](https://github.com/repolex-forx/psf--community-code-of-conduct) | `ebb4d2c1d4` | 2026-10-11 |
| [psf/elections](https://github.com/repolex-forx/psf--elections) | `68a6bfc258` | 2026-10-11 |
| [psf/user-success-wg](https://github.com/repolex-forx/psf--user-success-wg) | `16d552e3af` | 2026-10-11 |
| [pallets/werkzeug-website](https://github.com/repolex-forx/pallets--werkzeug-website) | `a1243ec510` | 2026-10-11 |
| [pallets/flask-ext-migrate](https://github.com/repolex-forx/pallets--flask-ext-migrate) | `913e598e60` | 2026-10-11 |
| [pallets/flask-sphinx-themes](https://github.com/repolex-forx/pallets--flask-sphinx-themes) | `3d562d0f68` | 2026-10-11 |
| [python-poetry/semver](https://github.com/repolex-forx/python-poetry--semver) | `7ef69b00f6` | 2026-10-11 |
| [tiangolo/tiangolo](https://github.com/repolex-forx/tiangolo--tiangolo) | `4e5408956f` | 2026-10-11 |
| [urllib3/urllib3-secure-extra](https://github.com/repolex-forx/urllib3--urllib3-secure-extra) | `b69da6320d` | 2026-10-11 |
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
