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
| [samuelcolvin/mkdocs-run-code](https://github.com/repolex-forx/samuelcolvin--mkdocs-run-code) | `9a39e6b22c` | 2026-10-11 |
| [samuelcolvin/mcpython](https://github.com/repolex-forx/samuelcolvin--mcpython) | `b461097e1d` | 2026-10-11 |
| [cherrypy/python3statement.github.io](https://github.com/repolex-forx/cherrypy--python3statement.github.io) | `ede803185d` | 2026-10-11 |
| [psf/bpo-tracker-cpython](https://github.com/repolex-forx/psf--bpo-tracker-cpython) | `1a94f0977c` | 2026-10-11 |
| [psf/python-in-edu](https://github.com/repolex-forx/psf--python-in-edu) | `d4634d5357` | 2026-10-11 |
| [psf/matterbridge-configuration](https://github.com/repolex-forx/psf--matterbridge-configuration) | `099868bb00` | 2026-10-11 |
| [psf/docker-mailman](https://github.com/repolex-forx/psf--docker-mailman) | `6b091fc17a` | 2026-10-11 |
| [pypa/packaging-problems](https://github.com/repolex-forx/pypa--packaging-problems) | `a4dd99101a` | 2026-10-11 |
| [pypa/rootbeer](https://github.com/repolex-forx/pypa--rootbeer) | `f121ac5e3b` | 2026-10-11 |
| [pypa/pip-test-package](https://github.com/repolex-forx/pypa--pip-test-package) | `96d6d72ac5` | 2026-10-11 |
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
