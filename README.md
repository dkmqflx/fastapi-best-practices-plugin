# fastapi-best-practices-plugin

A [Claude Code](https://claude.com/claude-code) plugin bundling a FastAPI best-practices skill — 41 rules across 13 categories, grounded in the official [FastAPI docs](https://fastapi.tiangolo.com/), prioritized by impact (security and correctness first, structure/validation/testing next, performance and polish last). Each rule pairs an incorrect example with the official correct pattern and links the relevant docs page.

## Install

```
/plugin marketplace add dkmqflx/fastapi-best-practices-plugin
/plugin install fastapi-best-practices@fastapi-best-practices-plugin
```

Then run `/reload-plugins`. The skill is model-invoked automatically based on context (writing endpoints, routers, dependencies, Pydantic models, error handling, auth, etc.) — you don't need to call it by name.

## Covers

Endpoints & `APIRouter`, query/path parameters, dependencies (`Depends`), Pydantic request/response models, error handling, `async def` vs `def`, lifespan events, security/auth, password hashing, streaming, background tasks, settings, testing, middleware, and CORS.

## Local development

```
claude --plugin-dir ./plugins/fastapi-best-practices
```

## License

MIT
