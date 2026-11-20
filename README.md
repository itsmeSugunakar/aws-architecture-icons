# AWS Architecture Icons

Mirror of AWS's official [Architecture Icons](https://aws.amazon.com/architecture/icons/)
asset package (Q3 2026 release, `07312026`), kept here as a stable public
host for tools (like [Archify](https://github.com/tt-a1i/archify)) that
need to fetch icons over HTTPS by digest-pinned URL rather than from a
local file.

**Usage terms**: per AWS's architecture-icons page, these assets may be
used to create architecture diagrams and incorporated into documents such
as whitepapers, presentations, data sheets, and posters.

## Layout

- `amazon-*.png`, `aws-*.png` (repo root) — a handful of individual icons
  pinned by URL + sha256 in specific diagrams. **Do not rename, move, or
  replace these files** — doing so breaks the digest pin for anything
  already referencing them (e.g. the architecture diagram in
  [conversation-analytics-app](https://github.com/itsmeSugunakar/conversation-analytics-app)).
- `full-package/` — the complete official package as downloaded:
  `Architecture-Service-Icons_*`, `Architecture-Group-Icons_*`,
  `Category-Icons_*`, `Resource-Icons_*`, each with `16/32/48/64` SVG/PNG
  variants (and `@5x` retina PNGs at the `64` size).

To pin a new icon from `full-package/` into a diagram, use its raw URL,
e.g.:

```
https://raw.githubusercontent.com/itsmeSugunakar/aws-architecture-icons/Dev/full-package/Architecture-Service-Icons_07312026/Arch_Compute/64/Arch_AWS-Lambda_64@5x.png
```

Archify's brand-capture only accepts raster images (PNG/JPEG/WebP), not
SVG, as of this writing.
