# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project — abstract syntax trees, dependency graphs, LSP-enriched semantic analysis, git history, and more — all queryable with SPARQL.

## [forx-index](https://github.com/repolex-forx/forx-index) — The Catalog

The **[forx-index](https://github.com/repolex-forx/forx-index)** repo is the central catalog of everything we've parsed. It contains JSON-LD manifests that form a lightweight knowledge graph: repositories, parsed commits, and the web of dependencies between projects. Load them into any RDF tool and query with SPARQL.

## Getting Started

Install [lexq](https://github.com/repolex-ai/lexq), the query tool for repolex knowledge graphs:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

Download a parsed repo:

```bash
lexq download repolex-ai/lexq
```

**lexq is designed to be used by LLMs in a terminal.** Start your favorite AI assistant and ask it to use lexq. It handles the SPARQL — you just ask questions in plain English.

```
"Claude, can you check the --help menu of lexq"
"Hermes, can you use the lexq tool to download someorg/somerepo"
"What classes are defined in this codebase?"
"Show me the dependency graph"
```

## Recently Parsed

<!-- AUTO-UPDATED BY FORX - DO NOT EDIT BELOW -->
| Data Source | Tag | Parsed |
|-------------|-----|--------|
| [pydantic/typing-inspection](https://github.com/repolex-forx/pydantic--typing-inspection) | v0.4.2 | 2026-09-16 |
| [sysid/sse-starlette](https://github.com/repolex-forx/sysid--sse-starlette) | 0.2.1 | 2026-09-16 |
| [open-telemetry/opentelemetry-python](https://github.com/repolex-forx/open-telemetry--opentelemetry-python) | v1.41.0 | 2026-09-16 |
| [pydantic/pydantic-settings](https://github.com/repolex-forx/pydantic--pydantic-settings) | v2.13.1 | 2026-09-16 |
| [openjdk/jdk](https://github.com/repolex-forx/openjdk--jdk) | jdk-26+15 | 2026-09-16 |
| [run-llama/llama_index](https://github.com/repolex-forx/run-llama--llama_index) | v0.12.32 | 2026-09-16 |
| [jpadilla/pyjwt](https://github.com/repolex-forx/jpadilla--pyjwt) | 2.12.1 | 2026-09-16 |
| [florimondmanca/httpx-sse](https://github.com/repolex-forx/florimondmanca--httpx-sse) | 0.4.3 | 2026-09-16 |
| [pygments/pygments](https://github.com/repolex-forx/pygments--pygments) | 2.0.1 | 2026-09-16 |
| [Kludex/python-multipart](https://github.com/repolex-forx/Kludex--python-multipart) | 0.0.24 | 2026-09-16 |
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

*Powered by [repolex](https://repolex.ai) · Orchestrated by [forx](https://github.com/repolex-ai/forx) · Queried with [lexq](https://github.com/repolex-ai/lexq)*
