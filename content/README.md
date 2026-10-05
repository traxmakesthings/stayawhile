# content

Everything I make that isn't code. It's all Markdown plus media, and the apps read it.

```
content/
├── thoughts/
│   └── 2026-10-05-slug.md
├── photos/
│   └── 2026-10-05-slug/
│       ├── index.md          caption, location, alt text
│       └── 01.jpg
├── videos/
│   └── 2026-10-05-slug/
│       ├── index.md          title, description, video URL
│       └── poster.jpg
└── work/
    └── project-slug/
        ├── index.md          the case study
        └── assets/
```

## Conventions

- **Slugs** are lowercase and hyphenated. Dated posts start with `YYYY-MM-DD-` so they sort chronologically.
- **Every post has frontmatter** with at least `title` and `date`. Add `draft: true` to keep a post unpublished.
- **Keep media next to the post that uses it.** Deleting a post folder should remove everything that belongs to it.

## Media

- **Photos:** commit images that have been exported for the web (a long edge of about 2400px is plenty). Keep camera originals out of the repo. Any folder named `originals/` is gitignored.
- **Videos:** don't commit video files, because they make git slow and the history can't be shrunk later. Upload them to a video host and put the URL in `index.md`. Only the poster image belongs in the repo.
