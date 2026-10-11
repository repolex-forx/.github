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
| [samuelcolvin/notify](https://github.com/repolex-forx/samuelcolvin--notify) | `128bf6230c` | 2026-10-11 |
| [samuelcolvin/python-devtools](https://github.com/repolex-forx/samuelcolvin--python-devtools) | `5022f1f6f1` | 2026-10-11 |
| [samuelcolvin/scratch](https://github.com/repolex-forx/samuelcolvin--scratch) | `09b89c9bd4` | 2026-10-11 |
| [samuelcolvin/array-has-slow](https://github.com/repolex-forx/samuelcolvin--array-has-slow) | `d833682ce9` | 2026-10-11 |
| [samuelcolvin/batson-perf](https://github.com/repolex-forx/samuelcolvin--batson-perf) | `107627c5ba` | 2026-10-11 |
| [samuelcolvin/mkdocs-redirects](https://github.com/repolex-forx/samuelcolvin--mkdocs-redirects) | `32ccfd0ce3` | 2026-10-11 |
| [samuelcolvin/aioaws](https://github.com/repolex-forx/samuelcolvin--aioaws) | `d4141e30a1` | 2026-10-11 |
| [samuelcolvin/pydantic-v2-startup-perf-bench](https://github.com/repolex-forx/samuelcolvin--pydantic-v2-startup-perf-bench) | `be3e062207` | 2026-10-11 |
| [samuelcolvin/ollama-python](https://github.com/repolex-forx/samuelcolvin--ollama-python) | `70dd0b7e63` | 2026-10-11 |
| [samuelcolvin/smokeshow](https://github.com/repolex-forx/samuelcolvin--smokeshow) | `6e982a3d08` | 2026-10-11 |
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
