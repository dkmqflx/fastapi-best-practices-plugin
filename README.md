# fastapi-best-practices-plugin

[![Release](https://img.shields.io/badge/release-v0.1.0-blue)](https://github.com/dkmqflx/fastapi-best-practices-plugin/releases/tag/fastapi-best-practices--v0.1.0)

3 FastAPI best-practice skills (41 rules total), grounded in the official [FastAPI docs](https://fastapi.tiangolo.com/). Security and testing are split into their own skills since they tend to live in dedicated files (auth modules, test suites) rather than alongside routing/model code. Each rule pairs an incorrect example with the official correct pattern and links the relevant docs page.

## Supported Coding Agents

These skills can be installed via [`npx skills`](https://github.com/vercel-labs/skills) for any agent that supports the [Agent Skills specification](https://skills.sh), including Claude Code, Codex, Gemini CLI, Cursor, Windsurf, and more.

## Install

### Quick Install (any supported agent)

Using [`npx skills`](https://github.com/vercel-labs/skills):

```bash
# Current project
npx skills add dkmqflx/fastapi-best-practices-plugin --skill '*' --yes

# All projects (global)
npx skills add dkmqflx/fastapi-best-practices-plugin --skill '*' --yes --global
```

To target a specific agent:

```bash
npx skills add dkmqflx/fastapi-best-practices-plugin --agent codex --skill '*' --yes
npx skills add dkmqflx/fastapi-best-practices-plugin --agent gemini-cli --skill '*' --yes
```

### Claude Code Plugin

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
