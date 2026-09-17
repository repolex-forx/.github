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
| [repolex-ai/git-lex](https://github.com/repolex-forx/repolex-ai--git-lex) | `26609d06d4` | 2026-09-17 |
| [repolex-ai/git-lex](https://github.com/repolex-forx/repolex-ai--git-lex) | `d6226dc2f9` | 2026-09-17 |
| [repolex-ai/git-lex](https://github.com/repolex-forx/repolex-ai--git-lex) | `4cab89d8e2` | 2026-09-17 |
| [openjdk/jdk](https://github.com/repolex-forx/openjdk--jdk) | jdk-26+15 | 2026-09-17 |
| [peritus/bumpversion](https://github.com/repolex-forx/peritus--bumpversion) | v0.5.3 | 2026-09-17 |
| [repolex-ai/rlex](https://github.com/repolex-forx/repolex-ai--rlex) | `22c79b34c8` | 2026-09-17 |
| [repolex-ai/forx](https://github.com/repolex-forx/repolex-ai--forx) | `8f9ab6f3bb` | 2026-09-17 |
| [repolex-ai/multilspy](https://github.com/repolex-forx/repolex-ai--multilspy) | `63e88426dc` | 2026-09-17 |
| [repolex-ai/rlex](https://github.com/repolex-forx/repolex-ai--rlex) | `bc7e632fa6` | 2026-09-17 |
| [repolex-ai/rlex](https://github.com/repolex-forx/repolex-ai--rlex) | `aa4df24901` | 2026-09-17 |
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
