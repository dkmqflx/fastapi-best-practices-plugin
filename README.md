# fastapi-best-practices-plugin

A [Claude Code](https://claude.com/claude-code) plugin bundling 3 FastAPI best-practice skills (41 rules total), grounded in the official [FastAPI docs](https://fastapi.tiangolo.com/). Security and testing are split into their own skills since they tend to live in dedicated files (auth modules, test suites) rather than alongside routing/model code. Each rule pairs an incorrect example with the official correct pattern and links the relevant docs page.

## Install

```
/plugin marketplace add dkmqflx/fastapi-best-practices-plugin
/plugin install fastapi-best-practices@fastapi-best-practices-plugin
```

Then run `/reload-plugins`. Skills are model-invoked automatically based on context — you don't need to call them by name.

## Skills

| Skill | Description |
|-------|-------------|
| `fastapi-best-practices` | Core guide — 33 rules across 11 categories: request/response models, params & validation, app structure & routing, DI, error handling, async, streaming, background tasks/config, lifespan, middleware, OpenAPI docs |
| `fastapi-security` | Security & auth — `OAuth2PasswordBearer`, `get_current_user` dependency, router-level auth, password hashing, token endpoint |
| `fastapi-testing` | Testing — `TestClient`, `dependency_overrides`, async `httpx` client |

## Local development

```
claude --plugin-dir ./plugins/fastapi-best-practices
```

## License

MIT
