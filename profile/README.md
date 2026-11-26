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
| [microsoft/windows-rs](https://github.com/repolex-forx/microsoft--windows-rs) | 0.20.1 | 2026-11-26 |
| [huggingface/peft](https://github.com/repolex-forx/huggingface--peft) | v0.15.0 | 2026-11-25 |
| [huggingface/tokenizers](https://github.com/repolex-forx/huggingface--tokenizers) | v0.13.4.rc3 | 2026-11-24 |
| [Azure/azure-sdk-for-python](https://github.com/repolex-forx/Azure--azure-sdk-for-python) | v2.0.0a1 | 2026-11-24 |
| [RustCrypto/traits](https://github.com/repolex-forx/RustCrypto--traits) | universal-hash-v0.6.1 | 2026-11-24 |
| [RustCrypto/utils](https://github.com/repolex-forx/RustCrypto--utils) | zeroize-v1.9.0 | 2026-11-24 |
| [RustCrypto/formats](https://github.com/repolex-forx/RustCrypto--formats) | x509-tsp/v0.1.0 | 2026-11-24 |
| [deedy5/primp](https://github.com/repolex-forx/deedy5--primp) | v0.15.0 | 2026-11-24 |
| [huggingface/xet-core](https://github.com/repolex-forx/huggingface--xet-core) | v20241218-00-dedup-upload-ctrlc | 2026-11-23 |
| [swc-project/swc-node](https://github.com/repolex-forx/swc-project--swc-node) | @swc-node/sourcemap-support@0.6.1 | 2026-11-23 |
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
