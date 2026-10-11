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
| [pypa/distlib](https://github.com/repolex-forx/pypa--distlib) | `454a87c64f` | 2026-10-11 |
| [tiangolo/sandbox](https://github.com/repolex-forx/tiangolo--sandbox) | `3dfd81eba4` | 2026-10-11 |
| [celery/celery-wheelhouse](https://github.com/repolex-forx/celery--celery-wheelhouse) | `fbe99121ac` | 2026-10-11 |
| [python-trio/trio-talks](https://github.com/repolex-forx/python-trio--trio-talks) | `184aeb818b` | 2026-10-11 |
| [python-trio/trio-ci-assets](https://github.com/repolex-forx/python-trio--trio-ci-assets) | `a4adf1b149` | 2026-10-11 |
| [psf/bpo-rietveld](https://github.com/repolex-forx/psf--bpo-rietveld) | `636b94cf73` | 2026-10-11 |
| [psf/psf-tuf-runbook](https://github.com/repolex-forx/psf--psf-tuf-runbook) | `01ff5b2b82` | 2026-10-11 |
| [pydantic/monty](https://github.com/repolex-forx/pydantic--monty) | `c6e072c41f` | 2026-10-11 |
| [tox-dev/velodex-data](https://github.com/repolex-forx/tox-dev--velodex-data) | `9a3a52f8ec` | 2026-10-11 |
| [litestar-org/branding](https://github.com/repolex-forx/litestar-org--branding) | `6a4f90f42d` | 2026-10-11 |
| [litestar-org/advanced-alchemy](https://github.com/repolex-forx/litestar-org--advanced-alchemy) | `e051a5de1a` | 2026-10-11 |
| [litestar-org/litestar-vite](https://github.com/repolex-forx/litestar-org--litestar-vite) | `5c49ec501d` | 2026-10-11 |
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
