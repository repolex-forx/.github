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
| [twisted/vertex](https://github.com/repolex-forx/twisted--vertex) | `feb591aa1b` | 2026-10-15 |
| [scrapy-plugins/scrapy-streamitem](https://github.com/repolex-forx/scrapy-plugins--scrapy-streamitem) | `78ecb9db71` | 2026-10-15 |
| [twisted/newsbuilder](https://github.com/repolex-forx/twisted--newsbuilder) | `5de0b3d90f` | 2026-10-15 |
| [twisted/quotient](https://github.com/repolex-forx/twisted--quotient) | `95f2515219` | 2026-10-15 |
| [twisted/mantissa](https://github.com/repolex-forx/twisted--mantissa) | `53e5502aba` | 2026-10-15 |
| [twisted/epsilon](https://github.com/repolex-forx/twisted--epsilon) | `68b7e43286` | 2026-10-15 |
| [twisted/nevow](https://github.com/repolex-forx/twisted--nevow) | `aff713a688` | 2026-10-15 |
| [twisted/axiom](https://github.com/repolex-forx/twisted--axiom) | `02a14c39ec` | 2026-10-15 |
| [twisted/qt5reactor](https://github.com/repolex-forx/twisted--qt5reactor) | `300a382b08` | 2026-10-15 |
| [twisted/twistedchecker](https://github.com/repolex-forx/twisted--twistedchecker) | `4a69f3f7d8` | 2026-10-15 |
| [executablebooks/mistletoe-ebp](https://github.com/repolex-forx/executablebooks--mistletoe-ebp) | `2298124367` | 2026-10-15 |
| [executablebooks/cli](https://github.com/repolex-forx/executablebooks--cli) | `4510602b43` | 2026-10-15 |
| [scrapy-plugins/scrapy-jsonrpc](https://github.com/repolex-forx/scrapy-plugins--scrapy-jsonrpc) | `15e0b7018c` | 2026-10-15 |
| [scrapy-plugins/scrapy-splash](https://github.com/repolex-forx/scrapy-plugins--scrapy-splash) | `72a8788212` | 2026-10-15 |
| [twisted/deferred](https://github.com/repolex-forx/twisted--deferred) | `d5f72e9068` | 2026-10-15 |
| [twisted/ampoule](https://github.com/repolex-forx/twisted--ampoule) | `58d3003cc8` | 2026-10-15 |
| [twisted/txacme](https://github.com/repolex-forx/twisted--txacme) | `ac18f92f6d` | 2026-10-15 |
| [twisted/txaws](https://github.com/repolex-forx/twisted--txaws) | `5c3317376c` | 2026-10-15 |
| [twisted/filepath](https://github.com/repolex-forx/twisted--filepath) | `920f6bb386` | 2026-10-15 |
| [twisted/tubes](https://github.com/repolex-forx/twisted--tubes) | `a28e91a08e` | 2026-10-15 |
| [sphinx-contrib/email](https://github.com/repolex-forx/sphinx-contrib--email) | `e23db323d1` | 2026-10-15 |
| [executablebooks/sphinx-globaltoc](https://github.com/repolex-forx/executablebooks--sphinx-globaltoc) | `ea6c5ad08c` | 2026-10-15 |
| [executablebooks/sphinx-yaml-config](https://github.com/repolex-forx/executablebooks--sphinx-yaml-config) | `b2339a3cd0` | 2026-10-15 |
| [executablebooks/github-activity](https://github.com/repolex-forx/executablebooks--github-activity) | `a73faf1082` | 2026-10-15 |
| [executablebooks/rst2myst](https://github.com/repolex-forx/executablebooks--rst2myst) | `32f1dd8a6b` | 2026-10-15 |
| [jupyter-server/enterprise_gateway](https://github.com/repolex-forx/jupyter-server--enterprise_gateway) | `880ab92b9a` | 2026-10-15 |
| [jupyter-server/synchronizer](https://github.com/repolex-forx/jupyter-server--synchronizer) | `faa25ac7ba` | 2026-10-15 |
| [jupyter-server/jupyter-scheduler](https://github.com/repolex-forx/jupyter-server--jupyter-scheduler) | `955883c1b3` | 2026-10-15 |
| [jupyter-server/fps](https://github.com/repolex-forx/jupyter-server--fps) | `b4e2d1f44f` | 2026-10-15 |
| [jupyter-server/jupyverse](https://github.com/repolex-forx/jupyter-server--jupyverse) | `5ab77dd10b` | 2026-10-15 |
| [sphinx-gallery/sphinx-gallery](https://github.com/repolex-forx/sphinx-gallery--sphinx-gallery) | `a7f3bac58f` | 2026-10-15 |
| [jupyter-server/jupyter_server_fileid](https://github.com/repolex-forx/jupyter-server--jupyter_server_fileid) | `c2902acd44` | 2026-10-15 |
| [jupyter-server/jupyter_releaser](https://github.com/repolex-forx/jupyter-server--jupyter_releaser) | `46ef93177d` | 2026-10-15 |
| [jupyter-server/gateway_provisioners](https://github.com/repolex-forx/jupyter-server--gateway_provisioners) | `d2d6f36c66` | 2026-10-15 |
| [jupyter-server/jupyter_server_mathjax](https://github.com/repolex-forx/jupyter-server--jupyter_server_mathjax) | `286f3852ae` | 2026-10-15 |
| [jupyter-server/jupyter_server_terminals](https://github.com/repolex-forx/jupyter-server--jupyter_server_terminals) | `46563c0797` | 2026-10-15 |
| [jupyter-server/pytest-jupyter](https://github.com/repolex-forx/jupyter-server--pytest-jupyter) | `9509dd22d3` | 2026-10-15 |
| [jupyter-server/kernel_gateway](https://github.com/repolex-forx/jupyter-server--kernel_gateway) | `8c483ff06e` | 2026-10-15 |
| [jupyter-server/jupyter_server](https://github.com/repolex-forx/jupyter-server--jupyter_server) | `f8169d721a` | 2026-10-15 |
| [celery/celery](https://github.com/repolex-forx/celery--celery) | `f5dbef3506` | 2026-10-15 |
| [sphinx-contrib/ansi](https://github.com/repolex-forx/sphinx-contrib--ansi) | `af63f758b1` | 2026-10-15 |
| [sphinx-contrib/datatemplates](https://github.com/repolex-forx/sphinx-contrib--datatemplates) | `2ad0b634fa` | 2026-10-15 |
| [jupyterhub/repo2docker](https://github.com/repolex-forx/jupyterhub--repo2docker) | `ebcc593885` | 2026-10-15 |
| [jupyterhub/binderhub](https://github.com/repolex-forx/jupyterhub--binderhub) | `1013493a4e` | 2026-10-15 |
| [jupyterhub/escapism](https://github.com/repolex-forx/jupyterhub--escapism) | `ae458c5ad9` | 2026-10-15 |
| [jupyterhub/sudospawner](https://github.com/repolex-forx/jupyterhub--sudospawner) | `304be890e2` | 2026-10-15 |
| [jupyterhub/jupyterhub](https://github.com/repolex-forx/jupyterhub--jupyterhub) | `10c37af3bf` | 2026-10-15 |
| [python-poetry/poetry](https://github.com/repolex-forx/python-poetry--poetry) | `38a86661d2` | 2026-10-15 |
| [boto/s3transfer](https://github.com/repolex-forx/boto--s3transfer) | `0ab921d7a0` | 2026-10-15 |
| [sphinx-contrib/video](https://github.com/repolex-forx/sphinx-contrib--video) | `4d04cefddc` | 2026-10-15 |
| [sphinx-contrib/fulltoc](https://github.com/repolex-forx/sphinx-contrib--fulltoc) | `8c09d8225e` | 2026-10-15 |
| [sphinx-contrib/redoc](https://github.com/repolex-forx/sphinx-contrib--redoc) | `5b9906bade` | 2026-10-15 |
| [sphinx-contrib/openapi](https://github.com/repolex-forx/sphinx-contrib--openapi) | `dd03c2bbaa` | 2026-10-15 |
| [jupyterhub/tmpauthenticator](https://github.com/repolex-forx/jupyterhub--tmpauthenticator) | `49cb1fb144` | 2026-10-15 |
| [jupyterhub/jupyter-server-proxy](https://github.com/repolex-forx/jupyterhub--jupyter-server-proxy) | `240a3ac397` | 2026-10-15 |
| [jupyterhub/wrapspawner](https://github.com/repolex-forx/jupyterhub--wrapspawner) | `cb74046aa0` | 2026-10-15 |
| [jupyterhub/simplespawner](https://github.com/repolex-forx/jupyterhub--simplespawner) | `86bd528fe1` | 2026-10-15 |
| [jupyterhub/dummyauthenticator](https://github.com/repolex-forx/jupyterhub--dummyauthenticator) | `6f0a5ea56f` | 2026-10-15 |
| [jupyterhub/kubespawner](https://github.com/repolex-forx/jupyterhub--kubespawner) | `47ce269d51` | 2026-10-15 |
| [pylint-dev/astroid](https://github.com/repolex-forx/pylint-dev--astroid) | `1eef6fa803` | 2026-10-15 |
| [pylint-dev/pylint-plugin-utils](https://github.com/repolex-forx/pylint-dev--pylint-plugin-utils) | `cee16e5e91` | 2026-10-15 |
| [pylint-dev/pylint-celery](https://github.com/repolex-forx/pylint-dev--pylint-celery) | `4edf639f29` | 2026-10-15 |
| [pylint-dev/pylint-django](https://github.com/repolex-forx/pylint-dev--pylint-django) | `370556a75a` | 2026-10-15 |
| [jupyterhub/firstuseauthenticator](https://github.com/repolex-forx/jupyterhub--firstuseauthenticator) | `7216c7415a` | 2026-10-15 |
| [jupyterhub/systemdspawner](https://github.com/repolex-forx/jupyterhub--systemdspawner) | `9a0a7f4efe` | 2026-10-15 |
| [jupyterhub/ldapauthenticator](https://github.com/repolex-forx/jupyterhub--ldapauthenticator) | `9d2759a3ca` | 2026-10-15 |
| [jupyterhub/batchspawner](https://github.com/repolex-forx/jupyterhub--batchspawner) | `451dcf171c` | 2026-10-15 |
| [jupyterhub/dockerspawner](https://github.com/repolex-forx/jupyterhub--dockerspawner) | `a73d0de667` | 2026-10-15 |
| [jupyterhub/oauthenticator](https://github.com/repolex-forx/jupyterhub--oauthenticator) | `02344def2a` | 2026-10-15 |
| [sphinx-contrib/images](https://github.com/repolex-forx/sphinx-contrib--images) | `fce459ff97` | 2026-10-15 |
| [sphinx-contrib/confluencebuilder](https://github.com/repolex-forx/sphinx-contrib--confluencebuilder) | `14515276dd` | 2026-10-15 |
| [sphinx-contrib/autoprogram](https://github.com/repolex-forx/sphinx-contrib--autoprogram) | `80ecc511c9` | 2026-10-15 |
| [colour-science/flask-compress](https://github.com/repolex-forx/colour-science--flask-compress) | `33ff4e5ebe` | 2026-10-15 |
| [vimalloc/flask-jwt-extended](https://github.com/repolex-forx/vimalloc--flask-jwt-extended) | `11785e00ea` | 2026-10-15 |
| [sphinx-contrib/spelling](https://github.com/repolex-forx/sphinx-contrib--spelling) | `1eb81816aa` | 2026-10-15 |
| [sphinx-contrib/httpdomain](https://github.com/repolex-forx/sphinx-contrib--httpdomain) | `32c21562d8` | 2026-10-15 |
| [spatialaudio/nbsphinx](https://github.com/repolex-forx/spatialaudio--nbsphinx) | `0d01427042` | 2026-10-15 |
| [googleapis/python-api-core](https://github.com/repolex-forx/googleapis--python-api-core) | `daf3040bef` | 2026-10-15 |
| [google/yapf](https://github.com/repolex-forx/google--yapf) | `1200509529` | 2026-10-15 |
| [click-contrib/click-log](https://github.com/repolex-forx/click-contrib--click-log) | `6e9ef98359` | 2026-10-15 |
| [click-contrib/click-datetime](https://github.com/repolex-forx/click-contrib--click-datetime) | `942964cf71` | 2026-10-15 |
| [click-contrib/click-repl](https://github.com/repolex-forx/click-contrib--click-repl) | `cab5f48382` | 2026-10-15 |
| [click-contrib/click-aliases](https://github.com/repolex-forx/click-contrib--click-aliases) | `8341453c07` | 2026-10-15 |
| [click-contrib/click-spinner](https://github.com/repolex-forx/click-contrib--click-spinner) | `31c253177d` | 2026-10-15 |
| [click-contrib/click-didyoumean](https://github.com/repolex-forx/click-contrib--click-didyoumean) | `d8a5eb9f82` | 2026-10-15 |
| [click-contrib/click-default-group](https://github.com/repolex-forx/click-contrib--click-default-group) | `dfddfd694e` | 2026-10-15 |
| [Textualize/frogmouth](https://github.com/repolex-forx/Textualize--frogmouth) | `15c3e85a6e` | 2026-10-15 |
| [Textualize/toolong](https://github.com/repolex-forx/Textualize--toolong) | `5aa22ee878` | 2026-10-15 |
| [Textualize/trogon](https://github.com/repolex-forx/Textualize--trogon) | `eaa9e68c40` | 2026-10-15 |
| [django-hijack/django-hijack](https://github.com/repolex-forx/django-hijack--django-hijack) | `c0bfe94e9f` | 2026-10-15 |
| [simonw/paginate-json](https://github.com/repolex-forx/simonw--paginate-json) | `4b4f5e6442` | 2026-10-15 |
| [simonw/llm-cluster](https://github.com/repolex-forx/simonw--llm-cluster) | `d2f93f1d17` | 2026-10-15 |
| [simonw/llm-ollama](https://github.com/repolex-forx/simonw--llm-ollama) | `4c91d4544a` | 2026-10-15 |
| [simonw/llm-cmd](https://github.com/repolex-forx/simonw--llm-cmd) | `1db3a14fdf` | 2026-10-15 |
| [simonw/llm-groq](https://github.com/repolex-forx/simonw--llm-groq) | `57be10aeb6` | 2026-10-15 |
| [encode/broadcaster](https://github.com/repolex-forx/encode--broadcaster) | `6b3ea71d4f` | 2026-10-15 |
| [encode/orm](https://github.com/repolex-forx/encode--orm) | `062f7e03d6` | 2026-10-15 |
| [encode/typesystem](https://github.com/repolex-forx/encode--typesystem) | `7decd48f40` | 2026-10-15 |
| [encode/databases](https://github.com/repolex-forx/encode--databases) | `ae3fb16f40` | 2026-10-15 |
| [tiangolo/asyncer](https://github.com/repolex-forx/tiangolo--asyncer) | `de024c755c` | 2026-10-15 |
| [piccolo-orm/piccolo_theme](https://github.com/repolex-forx/piccolo-orm--piccolo_theme) | `d6fad398aa` | 2026-10-15 |
| [piccolo-orm/piccolo_api](https://github.com/repolex-forx/piccolo-orm--piccolo_api) | `e1bee6cdda` | 2026-10-15 |
| [simonw/llm-claude-3](https://github.com/repolex-forx/simonw--llm-claude-3) | `5b42bfc3e5` | 2026-10-15 |
| [simonw/sqlite-dump](https://github.com/repolex-forx/simonw--sqlite-dump) | `14655bedf4` | 2026-10-15 |
| [simonw/yaml-to-sqlite](https://github.com/repolex-forx/simonw--yaml-to-sqlite) | `1405bc83c8` | 2026-10-15 |
| [simonw/files-to-prompt](https://github.com/repolex-forx/simonw--files-to-prompt) | `1b234ff6dc` | 2026-10-15 |
| [simonw/symbex](https://github.com/repolex-forx/simonw--symbex) | `81c4b9c042` | 2026-10-15 |
| [simonw/s3-credentials](https://github.com/repolex-forx/simonw--s3-credentials) | `4611f33340` | 2026-10-15 |
| [simonw/strip-tags](https://github.com/repolex-forx/simonw--strip-tags) | `868072957a` | 2026-10-15 |
| [adamchainz/django-mysql](https://github.com/repolex-forx/adamchainz--django-mysql) | `bb19ecea2d` | 2026-10-15 |
| [adamchainz/django-upgrade](https://github.com/repolex-forx/adamchainz--django-upgrade) | `4077de1d0f` | 2026-10-15 |
| [adamchainz/django-cors-headers](https://github.com/repolex-forx/adamchainz--django-cors-headers) | `8d96f0172c` | 2026-10-15 |
| [jieter/django-tables2](https://github.com/repolex-forx/jieter--django-tables2) | `34cdba3e13` | 2026-10-15 |
| [carltongibson/django-filter](https://github.com/repolex-forx/carltongibson--django-filter) | `daddf7b655` | 2026-10-15 |
| [jrief/django-admin-sortable2](https://github.com/repolex-forx/jrief--django-admin-sortable2) | `899402aa0a` | 2026-10-15 |
| [viewflow/django-fsm](https://github.com/repolex-forx/viewflow--django-fsm) | `88eeeca1a4` | 2026-10-15 |
| [django-guardian/django-guardian](https://github.com/repolex-forx/django-guardian--django-guardian) | `02465ce96c` | 2026-10-15 |
| [django-import-export/django-import-export](https://github.com/repolex-forx/django-import-export--django-import-export) | `6cdbaa3b49` | 2026-10-15 |
| [django-mptt/django-mptt](https://github.com/repolex-forx/django-mptt--django-mptt) | `72195e261d` | 2026-10-15 |
| [django-crispy-forms/django-crispy-forms](https://github.com/repolex-forx/django-crispy-forms--django-crispy-forms) | `e7fbb53859` | 2026-10-12 |
| [python-babel/flask-babel](https://github.com/repolex-forx/python-babel--flask-babel) | `869715cfea` | 2026-10-12 |
| [python-babel/babel](https://github.com/repolex-forx/python-babel--babel) | `e2a17919f0` | 2026-10-12 |
| [darrenburns/pytest-clarity](https://github.com/repolex-forx/darrenburns--pytest-clarity) | `533056491c` | 2026-10-12 |
| [ionelmc/pytest-benchmark](https://github.com/repolex-forx/ionelmc--pytest-benchmark) | `07d5196726` | 2026-10-12 |
| [Teemu/pytest-sugar](https://github.com/repolex-forx/Teemu--pytest-sugar) | `54ec9991e1` | 2026-10-12 |
| [glyph/automat](https://github.com/repolex-forx/glyph--automat) | `1e64bf3da9` | 2026-10-12 |
| [PyCQA/baron](https://github.com/repolex-forx/PyCQA--baron) | `eaa1062bec` | 2026-10-12 |
| [PyCQA/redbaron](https://github.com/repolex-forx/PyCQA--redbaron) | `9b4a1825d1` | 2026-10-12 |
| [PyCQA/prospector](https://github.com/repolex-forx/PyCQA--prospector) | `58a90fc31b` | 2026-10-12 |
| [python-restx/flask-restx](https://github.com/repolex-forx/python-restx--flask-restx) | `30abd919e7` | 2026-10-12 |
| [wtforms/wtforms](https://github.com/repolex-forx/wtforms--wtforms) | `ae8f4b4133` | 2026-10-12 |
| [PyCQA/astroid](https://github.com/repolex-forx/PyCQA--astroid) | `7716fe08e0` | 2026-10-12 |
| [PyCQA/doc8](https://github.com/repolex-forx/PyCQA--doc8) | `e4d2539177` | 2026-10-12 |
| [PyCQA/pydocstyle](https://github.com/repolex-forx/PyCQA--pydocstyle) | `8d0cdfc93e` | 2026-10-12 |
| [PyCQA/pycodestyle](https://github.com/repolex-forx/PyCQA--pycodestyle) | `96c007cb4e` | 2026-10-12 |
| [PyCQA/pyflakes](https://github.com/repolex-forx/PyCQA--pyflakes) | `de74d28a5f` | 2026-10-12 |
| [PyCQA/mccabe](https://github.com/repolex-forx/PyCQA--mccabe) | `292b5c71c3` | 2026-10-12 |
| [PyCQA/bandit](https://github.com/repolex-forx/PyCQA--bandit) | `68ebe11ef7` | 2026-10-12 |
| [PyCQA/flake8](https://github.com/repolex-forx/PyCQA--flake8) | `229f6c5387` | 2026-10-12 |
| [eventlet/eventlet](https://github.com/repolex-forx/eventlet--eventlet) | `d0111a51ce` | 2026-10-12 |
| [Tinche/aiofiles](https://github.com/repolex-forx/Tinche--aiofiles) | `3c2180f7f4` | 2026-10-12 |
| [aio-libs/async-timeout](https://github.com/repolex-forx/aio-libs--async-timeout) | `7dc0022fb8` | 2026-10-12 |
| [graphql-python/graphql-relay-py](https://github.com/repolex-forx/graphql-python--graphql-relay-py) | `611c0333ee` | 2026-10-12 |
| [python-openapi/openapi-schema-validator](https://github.com/repolex-forx/python-openapi--openapi-schema-validator) | `005e0804dd` | 2026-10-12 |
| [python-openapi/openapi-spec-validator](https://github.com/repolex-forx/python-openapi--openapi-spec-validator) | `2121137e48` | 2026-10-12 |
| [samuelcolvin/arq](https://github.com/repolex-forx/samuelcolvin--arq) | `5ee4b48cf6` | 2026-10-12 |
| [samuelcolvin/aiohttp-devtools](https://github.com/repolex-forx/samuelcolvin--aiohttp-devtools) | `5a5d4222c3` | 2026-10-12 |
| [lovasoa/marshmallow_dataclass](https://github.com/repolex-forx/lovasoa--marshmallow_dataclass) | `5c428f493e` | 2026-10-12 |
| [frankie567/httpx-oauth](https://github.com/repolex-forx/frankie567--httpx-oauth) | `8570ab5bff` | 2026-10-12 |
| [pydantic/logfire](https://github.com/repolex-forx/pydantic--logfire) | `199cc4df2d` | 2026-10-12 |
| [python-jsonschema/jsonschema-specifications](https://github.com/repolex-forx/python-jsonschema--jsonschema-specifications) | `5f06612cb4` | 2026-10-12 |
| [python-gitlab/python-gitlab](https://github.com/repolex-forx/python-gitlab--python-gitlab) | `51eb17e6e6` | 2026-10-12 |
| [python-jsonschema/check-jsonschema](https://github.com/repolex-forx/python-jsonschema--check-jsonschema) | `56b62a433c` | 2026-10-12 |
| [flask-restful/flask-restful](https://github.com/repolex-forx/flask-restful--flask-restful) | `88cce53a8c` | 2026-10-12 |
| [stefanfoulis/django-phonenumber-field](https://github.com/repolex-forx/stefanfoulis--django-phonenumber-field) | `5ef314efff` | 2026-10-12 |
| [django-ckeditor/django-ckeditor](https://github.com/repolex-forx/django-ckeditor--django-ckeditor) | `1a9c5a78ec` | 2026-10-12 |
| [pinax/pinax](https://github.com/repolex-forx/pinax--pinax) | `5a3b55788f` | 2026-10-12 |
| [stephenmcd/mezzanine](https://github.com/repolex-forx/stephenmcd--mezzanine) | `85dfd41244` | 2026-10-12 |
| [litestar-org/litestar](https://github.com/repolex-forx/litestar-org--litestar) | `afd3b039ab` | 2026-10-12 |
| [python-jsonschema/referencing](https://github.com/repolex-forx/python-jsonschema--referencing) | `40be109b70` | 2026-10-12 |
| [jpvanhal/inflection](https://github.com/repolex-forx/jpvanhal--inflection) | `88eefaacf7` | 2026-10-12 |
| [SmileyChris/django-countries](https://github.com/repolex-forx/SmileyChris--django-countries) | `a6462d30fa` | 2026-10-12 |
| [pypa/setuptools_scm](https://github.com/repolex-forx/pypa--setuptools_scm) | `6146a26063` | 2026-10-12 |
| [pypa/hatch](https://github.com/repolex-forx/pypa--hatch) | `7c26ebeaf8` | 2026-10-12 |
| [pypa/virtualenv](https://github.com/repolex-forx/pypa--virtualenv) | `a857a7823c` | 2026-10-12 |
| [jazzband/prettytable](https://github.com/repolex-forx/jazzband--prettytable) | `5fec60c0fd` | 2026-10-12 |
| [jazzband/django-oauth-toolkit](https://github.com/repolex-forx/jazzband--django-oauth-toolkit) | `c6e1bd2834` | 2026-10-12 |
| [jazzband/django-debug-toolbar](https://github.com/repolex-forx/jazzband--django-debug-toolbar) | `2ac540263e` | 2026-10-12 |
| [django-extensions/django-extensions](https://github.com/repolex-forx/django-extensions--django-extensions) | `9bdf315566` | 2026-10-12 |
| [piccolo-orm/piccolo_admin](https://github.com/repolex-forx/piccolo-orm--piccolo_admin) | `d6053adc9f` | 2026-10-12 |
| [piccolo-orm/piccolo](https://github.com/repolex-forx/piccolo-orm--piccolo) | `2556bbf2af` | 2026-10-12 |
| [tortoise/tortoise-orm](https://github.com/repolex-forx/tortoise--tortoise-orm) | `a47e3f6c9e` | 2026-10-12 |
| [maxcountryman/flask-login](https://github.com/repolex-forx/maxcountryman--flask-login) | `c8bba84b9b` | 2026-10-12 |
| [miguelgrinberg/Flask-Migrate](https://github.com/repolex-forx/miguelgrinberg--Flask-Migrate) | `bce4d35a0c` | 2026-10-12 |
| [corydolphin/flask-cors](https://github.com/repolex-forx/corydolphin--flask-cors) | `ad4f355791` | 2026-10-12 |
| [falconry/falcon](https://github.com/repolex-forx/falconry--falcon) | `05b35ee93d` | 2026-10-12 |
| [tiangolo/fastapi-cli](https://github.com/repolex-forx/tiangolo--fastapi-cli) | `093be9ca19` | 2026-10-12 |
| [tiangolo/sqlmodel](https://github.com/repolex-forx/tiangolo--sqlmodel) | `5ce1a47248` | 2026-10-12 |
| [tiangolo/typer](https://github.com/repolex-forx/tiangolo--typer) | `b15210b71a` | 2026-10-12 |
| [spec-first/swagger_ui_bundle](https://github.com/repolex-forx/spec-first--swagger_ui_bundle) | `77ce9d279b` | 2026-10-12 |
| [spec-first/connexion](https://github.com/repolex-forx/spec-first--connexion) | `a23d44e0e0` | 2026-10-12 |
| [executablebooks/jupyter-cache](https://github.com/repolex-forx/executablebooks--jupyter-cache) | `9394eada9b` | 2026-10-12 |
| [executablebooks/MyST-NB](https://github.com/repolex-forx/executablebooks--MyST-NB) | `23b1747ff9` | 2026-10-12 |
| [executablebooks/sphinx-exercise](https://github.com/repolex-forx/executablebooks--sphinx-exercise) | `9804d685b8` | 2026-10-12 |
| [executablebooks/sphinx-togglebutton](https://github.com/repolex-forx/executablebooks--sphinx-togglebutton) | `76bb31f882` | 2026-10-12 |
| [executablebooks/sphinx-proof](https://github.com/repolex-forx/executablebooks--sphinx-proof) | `d1113a8299` | 2026-10-12 |
| [executablebooks/sphinx-book-theme](https://github.com/repolex-forx/executablebooks--sphinx-book-theme) | `3512c865a6` | 2026-10-12 |
| [executablebooks/sphinx-thebe](https://github.com/repolex-forx/executablebooks--sphinx-thebe) | `60aa219f0a` | 2026-10-12 |
| [executablebooks/MyST-Parser](https://github.com/repolex-forx/executablebooks--MyST-Parser) | `723cffcf84` | 2026-10-12 |
| [strawberry-graphql/pytest-strawberry](https://github.com/repolex-forx/strawberry-graphql--pytest-strawberry) | `27ad06477d` | 2026-10-12 |
| [strawberry-graphql/strawberry-sqlalchemy](https://github.com/repolex-forx/strawberry-graphql--strawberry-sqlalchemy) | `e1ff9fd059` | 2026-10-12 |
| [strawberry-graphql/strawberry-django](https://github.com/repolex-forx/strawberry-graphql--strawberry-django) | `fd3f6502fc` | 2026-10-12 |
| [strawberry-graphql/strawberry](https://github.com/repolex-forx/strawberry-graphql--strawberry) | `0eb1c5ecb6` | 2026-10-12 |
| [executablebooks/sphinx-tabs](https://github.com/repolex-forx/executablebooks--sphinx-tabs) | `7e1d2eccd7` | 2026-10-12 |
| [executablebooks/rst-to-myst](https://github.com/repolex-forx/executablebooks--rst-to-myst) | `10d1edcb96` | 2026-10-12 |
| [executablebooks/mdit-py-plugins](https://github.com/repolex-forx/executablebooks--mdit-py-plugins) | `519953da0a` | 2026-10-12 |
| [executablebooks/sphinx-external-toc](https://github.com/repolex-forx/executablebooks--sphinx-external-toc) | `ba976dbe69` | 2026-10-12 |
| [executablebooks/mdurl](https://github.com/repolex-forx/executablebooks--mdurl) | `524d2edbbc` | 2026-10-12 |
| [executablebooks/sphinx-copybutton](https://github.com/repolex-forx/executablebooks--sphinx-copybutton) | `ef430062a3` | 2026-10-12 |
| [datasette/datasette-extract](https://github.com/repolex-forx/datasette--datasette-extract) | `4456f54f0c` | 2026-10-12 |
| [datasette/datasette-enrichments-llm](https://github.com/repolex-forx/datasette--datasette-enrichments-llm) | `40e7923095` | 2026-10-12 |
| [datasette/datasette-llm-usage](https://github.com/repolex-forx/datasette--datasette-llm-usage) | `a9269a8316` | 2026-10-12 |
| [datasette/datasette-referrer-policy](https://github.com/repolex-forx/datasette--datasette-referrer-policy) | `d70d80010b` | 2026-10-12 |
| [datasette/datasette-ip-rate-limit](https://github.com/repolex-forx/datasette--datasette-ip-rate-limit) | `8d338b0898` | 2026-10-12 |
| [datasette/datasette-pins](https://github.com/repolex-forx/datasette--datasette-pins) | `d865b27098` | 2026-10-12 |
| [datasette/datasette-comments](https://github.com/repolex-forx/datasette--datasette-comments) | `f381d96189` | 2026-10-12 |
| [datasette/datasette-auth-tailscale](https://github.com/repolex-forx/datasette--datasette-auth-tailscale) | `7520939af6` | 2026-10-12 |
| [datasette/datasette-tailscale](https://github.com/repolex-forx/datasette--datasette-tailscale) | `7f5ac3e3eb` | 2026-10-12 |
| [datasette/datasette-export-database](https://github.com/repolex-forx/datasette--datasette-export-database) | `ca3ba4fa05` | 2026-10-12 |
| [datasette/datasette-plugin-router](https://github.com/repolex-forx/datasette--datasette-plugin-router) | `63e93bafcc` | 2026-10-12 |
| [datasette/datasette-vite](https://github.com/repolex-forx/datasette--datasette-vite) | `e30144caef` | 2026-10-12 |
| [datasette/datasette-user-profiles](https://github.com/repolex-forx/datasette--datasette-user-profiles) | `5e0079532e` | 2026-10-12 |
| [datasette/datasette-places](https://github.com/repolex-forx/datasette--datasette-places) | `5429ce8edd` | 2026-10-12 |
| [datasette/datasette-files](https://github.com/repolex-forx/datasette--datasette-files) | `011d2106dc` | 2026-10-12 |
| [datasette/datasette-acl](https://github.com/repolex-forx/datasette--datasette-acl) | `b586db5bef` | 2026-10-12 |
| [datasette/datasette-agent-modeler](https://github.com/repolex-forx/datasette--datasette-agent-modeler) | `99844d7b50` | 2026-10-12 |
| [datasette/datasette-llm-limits](https://github.com/repolex-forx/datasette--datasette-llm-limits) | `c083b1d9fa` | 2026-10-12 |
| [datasette/datasette-public](https://github.com/repolex-forx/datasette--datasette-public) | `15585d8c79` | 2026-10-12 |
| [datasette/datasette-litestream](https://github.com/repolex-forx/datasette--datasette-litestream) | `6d043ddcaf` | 2026-10-12 |
| [datasette/datasette-mcp](https://github.com/repolex-forx/datasette--datasette-mcp) | `55f1ed1b74` | 2026-10-12 |
| [datasette/datasette-alerts](https://github.com/repolex-forx/datasette--datasette-alerts) | `c0a5fe7fbc` | 2026-10-12 |
| [datasette/datasette-agent](https://github.com/repolex-forx/datasette--datasette-agent) | `c811e82352` | 2026-10-12 |
| [datasette/datasette-cron](https://github.com/repolex-forx/datasette--datasette-cron) | `d90b8bd13d` | 2026-10-12 |
| [datasette/datasette-llm](https://github.com/repolex-forx/datasette--datasette-llm) | `b54d325aa3` | 2026-10-12 |
| [datasette/datasette-apps](https://github.com/repolex-forx/datasette--datasette-apps) | `f39519bfa8` | 2026-10-12 |
| [datasette/datasette-enrichments](https://github.com/repolex-forx/datasette--datasette-enrichments) | `76a4de39f5` | 2026-10-12 |
| [datasette/datasette-google-sheets](https://github.com/repolex-forx/datasette--datasette-google-sheets) | `51c5d380b7` | 2026-10-12 |
| [datasette/datasette-google-credentials](https://github.com/repolex-forx/datasette--datasette-google-credentials) | `c281379068` | 2026-10-12 |
| [datasette/datasette-accounts](https://github.com/repolex-forx/datasette--datasette-accounts) | `e3bd5c471f` | 2026-10-12 |
| [simonw/llm-gemini](https://github.com/repolex-forx/simonw--llm-gemini) | `e8de0b30d6` | 2026-10-12 |
| [simonw/llm-anthropic](https://github.com/repolex-forx/simonw--llm-anthropic) | `b66cdf112c` | 2026-10-12 |
| [simonw/llm-mistral](https://github.com/repolex-forx/simonw--llm-mistral) | `1b8807821f` | 2026-10-12 |
| [simonw/datasette-explain](https://github.com/repolex-forx/simonw--datasette-explain) | `d39ba0ff18` | 2026-10-12 |
| [simonw/datasette-atom](https://github.com/repolex-forx/simonw--datasette-atom) | `907ddfa520` | 2026-10-12 |
| [simonw/datasette-publish-fly](https://github.com/repolex-forx/simonw--datasette-publish-fly) | `a14b34ade8` | 2026-10-12 |
| [simonw/datasette-auth-github](https://github.com/repolex-forx/simonw--datasette-auth-github) | `1d47f69f5a` | 2026-10-12 |
| [simonw/datasette-block-robots](https://github.com/repolex-forx/simonw--datasette-block-robots) | `8470233830` | 2026-10-12 |
| [simonw/datasette-cluster-map](https://github.com/repolex-forx/simonw--datasette-cluster-map) | `d6b2362cbd` | 2026-10-12 |
| [simonw/datasette-auth-tokens](https://github.com/repolex-forx/simonw--datasette-auth-tokens) | `198f3af836` | 2026-10-12 |
| [Pylons/deformdemo](https://github.com/repolex-forx/Pylons--deformdemo) | `a54e82d97c` | 2026-10-12 |
| [Pylons/pyramid](https://github.com/repolex-forx/Pylons--pyramid) | `948c6bac3b` | 2026-10-12 |
| [fabric/patchwork](https://github.com/repolex-forx/fabric--patchwork) | `6768f7880c` | 2026-10-12 |
| [fabric/fabric](https://github.com/repolex-forx/fabric--fabric) | `ded51893f0` | 2026-10-12 |
| [simonw/csvs-to-sqlite](https://github.com/repolex-forx/simonw--csvs-to-sqlite) | `33b79ed80a` | 2026-10-12 |
| [simonw/shot-scraper](https://github.com/repolex-forx/simonw--shot-scraper) | `760c11449f` | 2026-10-12 |
| [simonw/ttok](https://github.com/repolex-forx/simonw--ttok) | `df24f50072` | 2026-10-12 |
| [simonw/datasette](https://github.com/repolex-forx/simonw--datasette) | `cf113a5985` | 2026-10-12 |
| [simonw/llm](https://github.com/repolex-forx/simonw--llm) | `05d7ae7ded` | 2026-10-12 |
| [simonw/sqlite-utils](https://github.com/repolex-forx/simonw--sqlite-utils) | `9c66bafa52` | 2026-10-12 |
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
