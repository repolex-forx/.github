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
| [cherrypy/cherrypy.github.io](https://github.com/repolex-forx/cherrypy--cherrypy.github.io) | `188d9e3db5` | 2026-10-11 |
| [psf/bpo-tracker-jython](https://github.com/repolex-forx/psf--bpo-tracker-jython) | `731b79d60e` | 2026-10-11 |
| [psf/bpo-tracker-roundup](https://github.com/repolex-forx/psf--bpo-tracker-roundup) | `88ef50697a` | 2026-10-11 |
| [cherrypy/tools](https://github.com/repolex-forx/cherrypy--tools) | `1b4e9438e9` | 2026-10-11 |
| [tiangolo/meinheld-gunicorn-docker](https://github.com/repolex-forx/tiangolo--meinheld-gunicorn-docker) | `70cb7974f4` | 2026-10-11 |
| [pallets/flask-docs](https://github.com/repolex-forx/pallets--flask-docs) | `ba4713af85` | 2026-10-11 |
| [psf/project-funding-wg](https://github.com/repolex-forx/psf--project-funding-wg) | `9c21a8c901` | 2026-10-11 |
| [psf/request-for](https://github.com/repolex-forx/psf--request-for) | `9f42ba4f02` | 2026-10-11 |
| [psf/fundable-packaging-improvements](https://github.com/repolex-forx/psf--fundable-packaging-improvements) | `638bbd48f4` | 2026-10-11 |
| [marshmallow-code/renovate-config](https://github.com/repolex-forx/marshmallow-code--renovate-config) | `b04c0a3af1` | 2026-10-11 |
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
