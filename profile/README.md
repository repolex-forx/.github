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
| [scrapy/formerly](https://github.com/repolex-forx/scrapy--formerly) | `1286733c17` | 2026-10-11 |
| [scrapy/scrapy-bench](https://github.com/repolex-forx/scrapy--scrapy-bench) | `48626327dc` | 2026-10-11 |
| [scrapy/slybot](https://github.com/repolex-forx/scrapy--slybot) | `47ce5afa74` | 2026-10-11 |
| [scrapy/pypydispatcher](https://github.com/repolex-forx/scrapy--pypydispatcher) | `3bee78abf2` | 2026-10-11 |
| [scrapy/dirbot](https://github.com/repolex-forx/scrapy--dirbot) | `8e99544736` | 2026-10-11 |
| [scrapy/scrapely](https://github.com/repolex-forx/scrapy--scrapely) | `31b5881bed` | 2026-10-11 |
| [scrapy/quotesbot](https://github.com/repolex-forx/scrapy--quotesbot) | `16ec3f4176` | 2026-10-11 |
| [scrapy/loginform](https://github.com/repolex-forx/scrapy--loginform) | `e61facef49` | 2026-10-11 |
| [scrapy/scrapyd-client](https://github.com/repolex-forx/scrapy--scrapyd-client) | `c6aa9d5817` | 2026-10-11 |
| [scrapy/xtractmime](https://github.com/repolex-forx/scrapy--xtractmime) | `9d50fcb0d7` | 2026-10-11 |
| [scrapy/scrapyd](https://github.com/repolex-forx/scrapy--scrapyd) | `50c4aa1d6e` | 2026-10-11 |
| [Pylons/weberror](https://github.com/repolex-forx/Pylons--weberror) | `8963e48ca7` | 2026-10-11 |
| [Pylons/pyramid_mailer](https://github.com/repolex-forx/Pylons--pyramid_mailer) | `2e6b72508d` | 2026-10-11 |
| [Pylons/pyramid_handlers](https://github.com/repolex-forx/Pylons--pyramid_handlers) | `b5023e666e` | 2026-10-11 |
| [Pylons/pyramid_ldap](https://github.com/repolex-forx/Pylons--pyramid_ldap) | `02aec38c80` | 2026-10-11 |
| [Pylons/pyramid_simpleform](https://github.com/repolex-forx/Pylons--pyramid_simpleform) | `30c666418c` | 2026-10-11 |
| [jupyterlab/jupyter-chat](https://github.com/repolex-forx/jupyterlab--jupyter-chat) | `977488a707` | 2026-10-11 |
| [requests/requests-threads](https://github.com/repolex-forx/requests--requests-threads) | `b4d4384da9` | 2026-10-11 |
| [requests/requests-kerberos](https://github.com/repolex-forx/requests--requests-kerberos) | `d4088c05ad` | 2026-10-11 |
| [requests/requests-ntlm](https://github.com/repolex-forx/requests--requests-ntlm) | `717339ff80` | 2026-10-11 |
| [requests/requests-oauthlib](https://github.com/repolex-forx/requests--requests-oauthlib) | `f33dac32bd` | 2026-10-11 |
| [jupyterlab/jupyter-ai](https://github.com/repolex-forx/jupyterlab--jupyter-ai) | `f7bf67342f` | 2026-10-11 |
| [jupyterlab/jupyterlab-git](https://github.com/repolex-forx/jupyterlab--jupyterlab-git) | `b62a87b719` | 2026-10-11 |
| [ipython/ipyparallel](https://github.com/repolex-forx/ipython--ipyparallel) | `d724f99d7e` | 2026-10-11 |
| [ipython/ipykernel](https://github.com/repolex-forx/ipython--ipykernel) | `a2b7a3ebbb` | 2026-10-11 |
| [pyca/ed25519](https://github.com/repolex-forx/pyca--ed25519) | `bc01a714d2` | 2026-10-11 |
| [pyca/pynacl](https://github.com/repolex-forx/pyca--pynacl) | `d869c68768` | 2026-10-11 |
| [pyca/bcrypt](https://github.com/repolex-forx/pyca--bcrypt) | `0e84f64b28` | 2026-10-11 |
| [twisted/pydoctor](https://github.com/repolex-forx/twisted--pydoctor) | `279e589afc` | 2026-10-11 |
| [twisted/ldaptor](https://github.com/repolex-forx/twisted--ldaptor) | `c3eaca5cdf` | 2026-10-11 |
| [ipython/comm](https://github.com/repolex-forx/ipython--comm) | `ba1c862a4c` | 2026-10-11 |
| [ipython/pickleshare](https://github.com/repolex-forx/ipython--pickleshare) | `9f0a267b02` | 2026-10-11 |
| [pyca/pyopenssl](https://github.com/repolex-forx/pyca--pyopenssl) | `567808adb4` | 2026-10-11 |
| [pyca/service-identity](https://github.com/repolex-forx/pyca--service-identity) | `6858d01dd8` | 2026-10-11 |
| [twisted/txmongo](https://github.com/repolex-forx/twisted--txmongo) | `128c88151f` | 2026-10-11 |
| [twisted/constantly](https://github.com/repolex-forx/twisted--constantly) | `c0ca511f6f` | 2026-10-11 |
| [twisted/incremental](https://github.com/repolex-forx/twisted--incremental) | `830ebeddf6` | 2026-10-11 |
| [twisted/treq](https://github.com/repolex-forx/twisted--treq) | `99f17121ab` | 2026-10-11 |
| [twisted/klein](https://github.com/repolex-forx/twisted--klein) | `722840bf1b` | 2026-10-11 |
| [twisted/towncrier](https://github.com/repolex-forx/twisted--towncrier) | `f92fbf5180` | 2026-10-11 |
| [Pylons/pyramid_zcml](https://github.com/repolex-forx/Pylons--pyramid_zcml) | `b7740dc319` | 2026-10-11 |
| [Pylons/pyramid_mako](https://github.com/repolex-forx/Pylons--pyramid_mako) | `7619ef2a5d` | 2026-10-11 |
| [Pylons/webob](https://github.com/repolex-forx/Pylons--webob) | `c0d70f985f` | 2026-10-11 |
| [Pylons/deform](https://github.com/repolex-forx/Pylons--deform) | `3977582583` | 2026-10-11 |
| [Pylons/pyramid_openapi3](https://github.com/repolex-forx/Pylons--pyramid_openapi3) | `39a3e77b75` | 2026-10-11 |
| [falconry/falcon-require-https](https://github.com/repolex-forx/falconry--falcon-require-https) | `1c1fd26aa7` | 2026-10-11 |
| [falconry/falcon-sync](https://github.com/repolex-forx/falconry--falcon-sync) | `c3a3eefdd8` | 2026-10-11 |
| [graphql-python/graphene-sqlalchemy](https://github.com/repolex-forx/graphql-python--graphene-sqlalchemy) | `4ea6ee8196` | 2026-10-11 |
| [graphql-python/graphene-federation](https://github.com/repolex-forx/graphql-python--graphene-federation) | `653357cf08` | 2026-10-11 |
| [graphql-python/graphene-mongo](https://github.com/repolex-forx/graphql-python--graphene-mongo) | `3b174a827f` | 2026-10-11 |
| [Pylons/webtest](https://github.com/repolex-forx/Pylons--webtest) | `938524c616` | 2026-10-11 |
| [Pylons/waitress](https://github.com/repolex-forx/Pylons--waitress) | `2b43237e9c` | 2026-10-11 |
| [falconry/falcon-oauthlib](https://github.com/repolex-forx/falconry--falcon-oauthlib) | `6e09a06bef` | 2026-10-11 |
| [falconry/falcon-mcp-server](https://github.com/repolex-forx/falconry--falcon-mcp-server) | `3cafe80225` | 2026-10-11 |
| [graphql-python/graphql-server](https://github.com/repolex-forx/graphql-python--graphql-server) | `2d5ac95393` | 2026-10-11 |
| [graphql-python/graphene-pydantic](https://github.com/repolex-forx/graphql-python--graphene-pydantic) | `2bc1b037db` | 2026-10-11 |
| [graphql-python/graphene-django](https://github.com/repolex-forx/graphql-python--graphene-django) | `0e6ef22a87` | 2026-10-11 |
| [graphql-python/gql](https://github.com/repolex-forx/graphql-python--gql) | `6ccc0cc2c2` | 2026-10-11 |
| [graphql-python/graphene](https://github.com/repolex-forx/graphql-python--graphene) | `8290326308` | 2026-10-11 |
| [graphql-python/graphql-core](https://github.com/repolex-forx/graphql-python--graphql-core) | `d913a6106f` | 2026-10-11 |
| [falconry/python-mimeparse](https://github.com/repolex-forx/falconry--python-mimeparse) | `76d2173365` | 2026-10-11 |
| [falconry/token-bucket](https://github.com/repolex-forx/falconry--token-bucket) | `75bc464c27` | 2026-10-11 |
| [pyinvoke/invocations](https://github.com/repolex-forx/pyinvoke--invocations) | `da97d736f9` | 2026-10-11 |
| [python-hyper/priority](https://github.com/repolex-forx/python-hyper--priority) | `532ace514d` | 2026-10-11 |
| [python-hyper/hyperlink](https://github.com/repolex-forx/python-hyper--hyperlink) | `978f2e6455` | 2026-10-11 |
| [python-hyper/hyperframe](https://github.com/repolex-forx/python-hyper--hyperframe) | `632e309bf6` | 2026-10-11 |
| [python-hyper/wsproto](https://github.com/repolex-forx/python-hyper--wsproto) | `5e0685d074` | 2026-10-11 |
| [python-hyper/hpack](https://github.com/repolex-forx/python-hyper--hpack) | `c2edbee3b5` | 2026-10-11 |
| [python-hyper/rfc3986](https://github.com/repolex-forx/python-hyper--rfc3986) | `3bd3832b72` | 2026-10-11 |
| [python-hyper/uritemplate](https://github.com/repolex-forx/python-hyper--uritemplate) | `4a38e9f6e7` | 2026-10-11 |
| [jazzband/django-mongonaut](https://github.com/repolex-forx/jazzband--django-mongonaut) | `6a008c7b8f` | 2026-10-11 |
| [jazzband/django-flatblocks](https://github.com/repolex-forx/jazzband--django-flatblocks) | `8ecea624a3` | 2026-10-11 |
| [jazzband/django-admin-sortable](https://github.com/repolex-forx/jazzband--django-admin-sortable) | `b9c1f3e0c4` | 2026-10-11 |
| [jazzband/django-ddp](https://github.com/repolex-forx/jazzband--django-ddp) | `1e1954b06f` | 2026-10-11 |
| [jazzband/django-postgres-utils](https://github.com/repolex-forx/jazzband--django-postgres-utils) | `886279ba1d` | 2026-10-11 |
| [jazzband/django-nose](https://github.com/repolex-forx/jazzband--django-nose) | `b90f7c96da` | 2026-10-11 |
| [jazzband/django-summernote](https://github.com/repolex-forx/jazzband--django-summernote) | `8b17863d44` | 2026-10-11 |
| [jazzband/pathlib2](https://github.com/repolex-forx/jazzband--pathlib2) | `0ac11b8d69` | 2026-10-11 |
| [jazzband/django-celery-monitor](https://github.com/repolex-forx/jazzband--django-celery-monitor) | `2b86acddc4` | 2026-10-11 |
| [jazzband/django-queued-storage](https://github.com/repolex-forx/jazzband--django-queued-storage) | `1cbb3c973e` | 2026-10-11 |
| [jazzband/django-tagging](https://github.com/repolex-forx/jazzband--django-tagging) | `79cb321b1e` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-serializinghtml](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-serializinghtml) | `f0f3b15b2e` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-devhelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-devhelp) | `0177fb44f1` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-applehelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-applehelp) | `f4f9d900b2` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-htmlhelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-htmlhelp) | `f7f5d4ecf2` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-qthelp](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-qthelp) | `783caf58e9` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-websupport](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-websupport) | `25dab08ff4` | 2026-10-11 |
| [sphinx-doc/sphinxext-rediraffe](https://github.com/repolex-forx/sphinx-doc--sphinxext-rediraffe) | `47273a20ad` | 2026-10-11 |
| [sphinx-doc/sphinxcontrib-django](https://github.com/repolex-forx/sphinx-doc--sphinxcontrib-django) | `0c06ad2379` | 2026-10-11 |
| [sphinx-doc/sphinx-argparse](https://github.com/repolex-forx/sphinx-doc--sphinx-argparse) | `32b9a006af` | 2026-10-11 |
| [sphinx-doc/alabaster](https://github.com/repolex-forx/sphinx-doc--alabaster) | `fba58a4398` | 2026-10-11 |
| [sphinx-doc/sphinxext-opengraph](https://github.com/repolex-forx/sphinx-doc--sphinxext-opengraph) | `95cf8a8c30` | 2026-10-11 |
| [sphinx-doc/sphinx-autobuild](https://github.com/repolex-forx/sphinx-doc--sphinx-autobuild) | `c9b7cb990e` | 2026-10-11 |
| [sphinx-doc/sphinx-intl](https://github.com/repolex-forx/sphinx-doc--sphinx-intl) | `1e9e8e9835` | 2026-10-11 |
| [aio-libs/create-aio-app](https://github.com/repolex-forx/aio-libs--create-aio-app) | `ece2a2b513` | 2026-10-11 |
| [aio-libs/sockjs](https://github.com/repolex-forx/aio-libs--sockjs) | `eeeb73568a` | 2026-10-11 |
| [aio-libs/aiopg](https://github.com/repolex-forx/aio-libs--aiopg) | `eabd5216c0` | 2026-10-11 |
| [aio-libs/aiozmq](https://github.com/repolex-forx/aio-libs--aiozmq) | `455faa6f93` | 2026-10-11 |
| [aio-libs/aiomysql](https://github.com/repolex-forx/aio-libs--aiomysql) | `1aa9cfcbad` | 2026-10-11 |
| [aio-libs/aiohttp-debugtoolbar](https://github.com/repolex-forx/aio-libs--aiohttp-debugtoolbar) | `f1ab053f57` | 2026-10-11 |
| [aio-libs/aiocache](https://github.com/repolex-forx/aio-libs--aiocache) | `ae5948b2d9` | 2026-10-11 |
| [aio-libs/janus](https://github.com/repolex-forx/aio-libs--janus) | `431248c05c` | 2026-10-11 |
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
