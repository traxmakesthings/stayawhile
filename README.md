# stayawhile

My corner of the internet: thoughts, photos, videos, product design work, and experiments.

This repo is a **monorepo**. Each deployable site lives in its own folder, shared code lives in `packages/`, and everything I write or shoot lives in `content/`, kept separate from the code that displays it.

```
stayawhile/
├── apps/
│   └── web/                  → domain.com        (the main site)
├── experiments/
│   ├── _template/            → starting point for new experiments (never deployed)
│   └── <slug>/               → <slug>.domain.com
├── packages/
│   ├── ui/                   shared components
│   ├── tokens/               design tokens: color, type, spacing, motion
│   └── config/               shared tooling config (tsconfig, lint, format)
├── content/
│   ├── thoughts/             writing
│   ├── photos/               photo posts
│   ├── videos/               video posts
│   └── work/                 portfolio case studies
└── docs/
    └── decisions/            short records of why things are the way they are
```

## Rules

1. **One folder = one deployable.** Anything in `apps/` or `experiments/` builds and deploys on its own. The experiment's folder name is its subdomain.
2. **Content is data, not code.** `content/` holds Markdown and media only. Apps read from it, so a redesign never means rewriting posts.
3. **Share through `packages/`, never sideways.** An experiment can import `packages/ui`, but it never imports from `apps/web` or from another experiment. This keeps every experiment deletable.
4. **Folders starting with `_` aren't deployed.**

## Naming

| What | Format | Example |
|---|---|---|
| Experiment folder (= subdomain) | lowercase `a-z`, `0-9`, `-`; max 63 chars | `26daysoftype` |
| Thought | `YYYY-MM-DD-slug.md` | `2026-10-05-why-i-made-this.md` |
| Photo / video post | `YYYY-MM-DD-slug/` folder with `index.md` | `2026-10-05-kyoto/` |
| Case study | `project-slug/` folder with `index.md` | `checkout-redesign/` |

See each folder's README for details. To start a new experiment, read [`experiments/README.md`](experiments/README.md).
