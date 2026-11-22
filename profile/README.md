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
| [regebro/pyroma](https://github.com/repolex-forx/regebro--pyroma) | 5.0.1 | 2026-11-22 |
| [sphinx-doc/sphinx-autobuild](https://github.com/repolex-forx/sphinx-doc--sphinx-autobuild) | v0.7.1 | 2026-11-22 |
| [stefankoegl/python-json-pointer](https://github.com/repolex-forx/stefankoegl--python-json-pointer) | v3.1.1 | 2026-11-22 |
| [dvarrazzo/py-setproctitle](https://github.com/repolex-forx/dvarrazzo--py-setproctitle) | version-1.3.7 | 2026-11-22 |
| [nvzqz/static-assertions-rs](https://github.com/repolex-forx/nvzqz--static-assertions-rs) | v1.1.0 | 2026-11-22 |
| [dtolnay/trybuild](https://github.com/repolex-forx/dtolnay--trybuild) | 1.0.116 | 2026-11-22 |
| [rust-openssl/rust-openssl](https://github.com/repolex-forx/rust-openssl--rust-openssl) | v0.9.23 | 2026-11-22 |
| [tafia/quick-xml](https://github.com/repolex-forx/tafia--quick-xml) | v0.39.2 | 2026-11-22 |
| [pydantic/speedate](https://github.com/repolex-forx/pydantic--speedate) | v0.17.0 | 2026-11-22 |
| [pytest-dev/pyfakefs](https://github.com/repolex-forx/pytest-dev--pyfakefs) | v6.2.0 | 2026-11-22 |
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
