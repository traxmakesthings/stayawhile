# packages

Code that more than one app or experiment uses.

| Package | Contents |
|---|---|
| `tokens/` | Design tokens (color, type, spacing, motion). This is the single source of truth for the visual language. |
| `ui/` | Shared components built on `tokens`. |
| `config/` | Shared tooling config (TypeScript, lint, format) that apps extend. |

Only move something here once a second consumer needs it. Until then, keep it in the app that uses it.
