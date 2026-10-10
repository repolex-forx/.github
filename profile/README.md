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
| [vllm-project/humming](https://github.com/repolex-forx/vllm-project--humming) | `f08e744fb1` | 2026-10-10 |
| [psf/diversity-and-inclusion-wg](https://github.com/repolex-forx/psf--diversity-and-inclusion-wg) | `73b21b9dc5` | 2026-10-10 |
| [BerriAI/litellm-lens-example](https://github.com/repolex-forx/BerriAI--litellm-lens-example) | `238d61d611` | 2026-10-10 |
| [psf/black-pre-commit-mirror](https://github.com/repolex-forx/psf--black-pre-commit-mirror) | 26.10.1 | 2026-10-10 |
| [sgl-project/SpecForge](https://github.com/repolex-forx/sgl-project--SpecForge) | `fdcc2eddf1` | 2026-10-10 |
| [BerriAI/litellm-memory](https://github.com/repolex-forx/BerriAI--litellm-memory) | `283454d073` | 2026-10-10 |
| [psf/pyperf](https://github.com/repolex-forx/psf--pyperf) | `00556e1877` | 2026-10-10 |
| [BerriAI/ai-gateway-bench](https://github.com/repolex-forx/BerriAI--ai-gateway-bench) | `35ba690a53` | 2026-10-10 |
| [psf/pypistats.org](https://github.com/repolex-forx/psf--pypistats.org) | `2a433267de` | 2026-10-10 |
| [psf/cachecontrol](https://github.com/repolex-forx/psf--cachecontrol) | `2627d9b267` | 2026-10-10 |
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
