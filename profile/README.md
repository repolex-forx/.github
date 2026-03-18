# repolex-forx

**Source code as a knowledge graph.** Every repo here contains RDF graph data parsed from an open source project - abstract syntax trees, git history, semantic analysis, and more, queryable with SPARQL.

## What is this?

Each repository in this org is a parsed representation of an open source project. For example, [`repolex-ai--lexq`](https://github.com/repolex-forx/repolex-ai--lexq) contains the full knowledge graph of [repolex-ai/lexq](https://github.com/repolex-ai/lexq).

## Quick start

Install the [lexq](https://github.com/repolex-ai/lexq) query tool:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

Download and query any repo:

```bash
lexq download repolex-ai/lexq
lexq query "SELECT ?class WHERE { ?class a ast:ClassDeclaration }"
```

lexq is designed to be used primarily by LLMs in a terminal. Start up your favorite LLM and ask it to use the lexq tool.

## Parsed repositories

<!-- This section will be auto-updated by forx update-index -->

| Source | Knowledge Graph | Language |
|--------|----------------|----------|
| [TopQuadrant/shacl](https://github.com/TopQuadrant/shacl) | [TopQuadrant--shacl](https://github.com/repolex-forx/TopQuadrant--shacl) | Java |
| [pallets/flask](https://github.com/pallets/flask) | [pallets--flask](https://github.com/repolex-forx/pallets--flask) | Python |
| [psf/requests](https://github.com/psf/requests) | [psf--requests](https://github.com/repolex-forx/psf--requests) | Python |
| [Textualize/rich](https://github.com/Textualize/rich) | [Textualize--rich](https://github.com/repolex-forx/Textualize--rich) | Python |
| [expressjs/express](https://github.com/expressjs/express) | [expressjs--express](https://github.com/repolex-forx/expressjs--express) | JavaScript |
| [colinhacks/zod](https://github.com/colinhacks/zod) | [colinhacks--zod](https://github.com/repolex-forx/colinhacks--zod) | TypeScript |
| [trpc/trpc](https://github.com/trpc/trpc) | [trpc--trpc](https://github.com/repolex-forx/trpc--trpc) | TypeScript |
| [serde-rs/serde](https://github.com/serde-rs/serde) | [serde-rs--serde](https://github.com/repolex-forx/serde-rs--serde) | Rust |
| [gin-gonic/gin](https://github.com/gin-gonic/gin) | [gin-gonic--gin](https://github.com/repolex-forx/gin-gonic--gin) | Go |
| [rack/rack](https://github.com/rack/rack) | [rack--rack](https://github.com/repolex-forx/rack--rack) | Ruby |
| [dart-lang/http](https://github.com/dart-lang/http) | [dart-lang--http](https://github.com/repolex-forx/dart-lang--http) | Dart |
| [JamesNK/Newtonsoft.Json](https://github.com/JamesNK/Newtonsoft.Json) | [JamesNK--Newtonsoft.Json](https://github.com/repolex-forx/JamesNK--Newtonsoft.Json) | C# |
| [pixeltable/pixeltable](https://github.com/pixeltable/pixeltable) | [pixeltable--pixeltable](https://github.com/repolex-forx/pixeltable--pixeltable) | Python |
| ...and more | | |

> This data is experimental and subject to change without notice.

---

*Powered by [repolex](https://repolex.ai)*
