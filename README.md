# rechedev-plugins

Marketplace personal de plugins para [Claude Code](https://claude.com/claude-code).

## Plugins incluidos

| Plugin | Descripción |
| --- | --- |
| [superpowers](https://github.com/rechedev9/superpowers) | Fork personal de [obra/superpowers](https://github.com/obra/superpowers): brainstorming, subagent-driven development, code review, systematic debugging y red/green TDD. |

## Cómo usarlo

Desde Claude Code:

```
/plugin marketplace add rechedev9/rechedev-plugins
/plugin install superpowers@rechedev-plugins
```

## Actualizar la versión de un plugin

1. Hacer cambios en el repo del plugin (por ejemplo, `rechedev9/superpowers`).
2. Actualizar el campo `sha` del plugin en `.claude-plugin/marketplace.json` apuntando al nuevo commit.
3. Commit y push de este repo.
4. En Claude Code: `/plugin marketplace update rechedev-plugins`.

## Añadir un plugin nuevo

Edita `.claude-plugin/marketplace.json` y añade una entrada al array `plugins`. Estructura mínima:

```json
{
  "name": "nombre-del-plugin",
  "description": "Qué hace",
  "category": "development",
  "source": {
    "source": "url",
    "url": "https://github.com/usuario/repo.git",
    "sha": "<commit-sha>"
  },
  "homepage": "https://github.com/usuario/repo"
}
```

## Licencia

MIT — ver `LICENSE`.
