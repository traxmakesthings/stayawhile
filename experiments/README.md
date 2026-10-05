# experiments

Each folder is a standalone site served on its own subdomain:

```
experiments/<slug>/  →  <slug>.domain.com
```

## Starting a new experiment

1. Copy `_template/` to `experiments/<slug>/`.
2. Make sure `<slug>` is a valid subdomain: lowercase `a-z`, `0-9` and `-` only, can't start or end with `-`, 63 characters max.
3. Fill in the experiment's `README.md` (what it is, its status, dates).
4. Give it its own deploy project and point `<slug>.domain.com` at it.

## Rules

- **Self-contained.** An experiment can import from `packages/*`, but not from `apps/` or from other experiments. You should be able to delete the folder without breaking anything else.
- **Pick any stack.** Each experiment manages its own dependencies, so one can use React and the next can be plain HTML.
- **Folders starting with `_` aren't deployed.**

## Index

| Slug | Subdomain | Status |
|---|---|---|
| | | |

_No experiments yet. Add a row whenever you create one._
