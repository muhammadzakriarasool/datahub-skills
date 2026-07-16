# datahub-pipeline-generate Skill

Generate production pipeline code (dbt models, SQL transformations, orchestration DAGs) grounded in real DataHub metadata — with bidirectional metadata write-back.

## What it does

1. **Discovers** target entities in DataHub (by name or URN)
2. **Collects context** — schema, lineage, ownership, tags, glossary terms, quality health
3. **Generates code** — dbt models, SQL transformations, Airflow/Dagster DAGs with real column names, types, and platform dialects
4. **Writes back** — tags (`generated-by-autopipeline`, `needs-review`), descriptions, glossary terms, and ownership back to the DataHub graph

## Directory structure

```
skills/datahub-pipeline-generate/
  SKILL.md              # Main skill definition (frontmatter + comprehensive markdown)
  references/            # Platform-specific reference docs
  templates/             # Code generation templates
  README.md              # This file
```

## Usage

This skill is designed for multi-agent compatibility (Claude Code, Cursor, Codex, Copilot, Gemini CLI, Windsurf, and MCP-compatible agents). Load via `skill_view(name='datahub-pipeline-generate')`.

## See also

- `/datahub-search` — Discover entities
- `/datahub-lineage` — Explore lineage patterns
- `/datahub-enrich` — Batch metadata updates
- `/datahub-quality` — Quality assertions and incidents
- `/datahub-setup` — CLI installation and authentication
