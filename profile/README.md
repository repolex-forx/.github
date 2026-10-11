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
| [pallets-eco/.github](https://github.com/repolex-forx/pallets-eco--.github) | `aa505cc7ea` | 2026-10-11 |
| [pytest-dev/pytest-issue-2419](https://github.com/repolex-forx/pytest-dev--pytest-issue-2419) | `1eab7a9c7a` | 2026-10-11 |
| [samuelcolvin/basedpyright-zed](https://github.com/repolex-forx/samuelcolvin--basedpyright-zed) | `a6012ade8a` | 2026-10-11 |
| [samuelcolvin/awesome-mcp-servers](https://github.com/repolex-forx/samuelcolvin--awesome-mcp-servers) | `beb8dc051b` | 2026-10-11 |
| [samuelcolvin/logfire-go-logs](https://github.com/repolex-forx/samuelcolvin--logfire-go-logs) | `8b3eba6d2f` | 2026-10-11 |
| [samuelcolvin/uk-parliament-relatives](https://github.com/repolex-forx/samuelcolvin--uk-parliament-relatives) | `7b7e9e8090` | 2026-10-11 |
| [samuelcolvin/pull_pull_request](https://github.com/repolex-forx/samuelcolvin--pull_pull_request) | `74df6a76a3` | 2026-10-11 |
| [tox-dev/tox-tags](https://github.com/repolex-forx/tox-dev--tox-tags) | `c9968c0de9` | 2026-10-11 |
| [cherrypy/.github](https://github.com/repolex-forx/cherrypy--.github) | `c0263bf269` | 2026-10-11 |
| [marshmallow-code/.github](https://github.com/repolex-forx/marshmallow-code--.github) | `c95e0c1a38` | 2026-10-11 |
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
