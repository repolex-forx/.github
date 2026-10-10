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
| [honojs/cli](https://github.com/repolex-forx/honojs--cli) | `c1b6028d8e` | 2026-10-10 |
| [honojs/agent-dx](https://github.com/repolex-forx/honojs--agent-dx) | `8e85e3c3e8` | 2026-10-10 |
| [drizzle-team/brocli](https://github.com/repolex-forx/drizzle-team--brocli) | 0.12.1 | 2026-10-10 |
| [BerriAI/liteadmin-mcp](https://github.com/repolex-forx/BerriAI--liteadmin-mcp) | `d35ec9c19c` | 2026-10-10 |
| [BerriAI/litellm-admin-agent](https://github.com/repolex-forx/BerriAI--litellm-admin-agent) | `3fdd3d3390` | 2026-10-10 |
| [drizzle-team/hanji](https://github.com/repolex-forx/drizzle-team--hanji) | `9643039148` | 2026-10-10 |
| [honojs/create-hono](https://github.com/repolex-forx/honojs--create-hono) | v0.20.0-rc.0 | 2026-10-10 |
| [honojs/skills](https://github.com/repolex-forx/honojs--skills) | `5becff4242` | 2026-10-10 |
| [vllm-project/humming](https://github.com/repolex-forx/vllm-project--humming) | `f08e744fb1` | 2026-10-10 |
| [psf/diversity-and-inclusion-wg](https://github.com/repolex-forx/psf--diversity-and-inclusion-wg) | `73b21b9dc5` | 2026-10-10 |
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
