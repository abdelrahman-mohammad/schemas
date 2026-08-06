# schemas

Public JSON Schemas for my tooling, served by GitHub Pages so editors can resolve them.

| Schema | URL |
| --- | --- |
| `pipeline.schema.json` | <https://abdelrahman-mohammad.github.io/schemas/pipeline.schema.json> |

## pipeline.schema.json

Validates `.claude/pipeline.json`, the per-repository contract read by
[claude-pipeline](https://github.com/abdelrahman-mohammad/claude-pipeline) — its hooks and its
skills both read the same file, so they cannot disagree about what a repo has opted into.

Reference it from a config with:

```json
{ "$schema": "https://abdelrahman-mohammad.github.io/schemas/pipeline.schema.json", "version": 1 }
```

Only `version` is required. The presence of `branches` is what marks a repository as onboarded.
