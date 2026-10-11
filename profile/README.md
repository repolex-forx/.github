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
| [pallets-eco/flask-docs-translations](https://github.com/repolex-forx/pallets-eco--flask-docs-translations) | `71e4a78866` | 2026-10-10 |
| [samuelcolvin/scolvin.com](https://github.com/repolex-forx/samuelcolvin--scolvin.com) | `fe642c11e1` | 2026-10-10 |
| [samuelcolvin/obsbot-rs](https://github.com/repolex-forx/samuelcolvin--obsbot-rs) | `e8a17fb8f1` | 2026-10-10 |
| [tornadoweb/tornado-testbed](https://github.com/repolex-forx/tornadoweb--tornado-testbed) | `ba2cc54671` | 2026-10-10 |
| [pypa/manylinux](https://github.com/repolex-forx/pypa--manylinux) | `57bd9a6e8f` | 2026-10-10 |
| [psf/webassembly](https://github.com/repolex-forx/psf--webassembly) | `60cd7a6672` | 2026-10-10 |
| [psf/sboms-for-python-packages](https://github.com/repolex-forx/psf--sboms-for-python-packages) | `a399bc2f1e` | 2026-10-10 |
| [psf/policies](https://github.com/repolex-forx/psf--policies) | `e767816f96` | 2026-10-10 |
| [psf/organizer-toolkit](https://github.com/repolex-forx/psf--organizer-toolkit) | `661a39b6b0` | 2026-10-10 |
| [psf/requests-html](https://github.com/repolex-forx/psf--requests-html) | `075ac162dc` | 2026-10-10 |
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
