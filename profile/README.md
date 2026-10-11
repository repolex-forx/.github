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
| [python-trio/trzmq](https://github.com/repolex-forx/python-trio--trzmq) | `275ce1d927` | 2026-10-11 |
| [samuelcolvin/email-me](https://github.com/repolex-forx/samuelcolvin--email-me) | `c1c8260672` | 2026-10-11 |
| [samuelcolvin/MacTab](https://github.com/repolex-forx/samuelcolvin--MacTab) | `e03917f222` | 2026-10-11 |
| [cherrypy/tools-legacy](https://github.com/repolex-forx/cherrypy--tools-legacy) | `f9f5337c85` | 2026-10-11 |
| [bottlepy/bottle-memcache](https://github.com/repolex-forx/bottlepy--bottle-memcache) | `1d4ed714cc` | 2026-10-11 |
| [bottlepy/bottle-beaker](https://github.com/repolex-forx/bottlepy--bottle-beaker) | `37ccd0f0db` | 2026-10-11 |
| [bottlepy/bottle-werkzeug](https://github.com/repolex-forx/bottlepy--bottle-werkzeug) | `77361e3e03` | 2026-10-11 |
| [bottlepy/bottle-boilerplate](https://github.com/repolex-forx/bottlepy--bottle-boilerplate) | `097a044d93` | 2026-10-11 |
| [bottlepy/bottle-redis](https://github.com/repolex-forx/bottlepy--bottle-redis) | `4c2306e5c8` | 2026-10-11 |
| [bottlepy/bottle-inject](https://github.com/repolex-forx/bottlepy--bottle-inject) | `321d7f45be` | 2026-10-11 |
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
