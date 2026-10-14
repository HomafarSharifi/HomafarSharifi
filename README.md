# Roadmap-first GitHub profile README

An editable GitHub profile README system for a developing software engineer with a product-design mindset. The visual language pairs dark charcoal surfaces with electric blue highlights, minimal line icons, and a clear learning path.

> Replace the sample name, handle, and links before publishing. This system intentionally has no project showcase section.

## Preview and structure

The profile is designed as a sequence: identity → current focus → roadmap → ways to connect. Keep the roadmap as the primary content. Use the assets in `assets/` as source artwork, then export optimized SVG or PNG files if your profile needs hosted images.

```text
roadmap-readme-design-system/
├── README.md
├── DESIGN-GUIDE.md
├── CUSTOMIZATION-CHECKLIST.md
├── assets/
│   ├── design-tokens.css
│   ├── hero.svg
│   ├── roadmap.svg
│   └── divider.svg
└── docs/
    └── README-EXAMPLE.md
```

## Quick start

1. Open `docs/README-EXAMPLE.md` and personalize its profile fields and focus statement.
2. Open SVG artwork in Figma (or a vector editor) to change the composition, line icons, and labels.
3. Keep colors aligned with `assets/design-tokens.css` and the token table in `DESIGN-GUIDE.md`.
4. Export the artwork to your profile repository, usually as `assets/profile-hero.svg`, `assets/roadmap.svg`, and `assets/divider.svg`.
5. Copy the example into the profile repository's root `README.md`, update the image paths, and preview it on GitHub.

GitHub profile READMEs are Markdown, so the SVGs must be committed to a public repository or otherwise hosted at URLs GitHub can access. Test SVG rendering in the GitHub preview after export.

## Customization map

| Want to change | Edit |
| --- | --- |
| Charcoal, blue, text, or border colors | `assets/design-tokens.css`; then update matching SVG attributes or use Figma's color styles |
| Hero headline, subtitle, or identity | `assets/hero.svg` and `docs/README-EXAMPLE.md` |
| Roadmap steps, icons, or current stage | `assets/roadmap.svg` and the roadmap section in the example |
| Separator weight and color | `assets/divider.svg` |
| Layout/export/publishing decisions | `DESIGN-GUIDE.md` |
| Final pre-publish checks | `CUSTOMIZATION-CHECKLIST.md` |

## Design principles

- **Roadmap first:** show the direction and current stage before any optional profile details.
- **Product mindset:** connect engineering foundations to useful products and thoughtful experiences.
- **Minimal line icons:** consistent stroke weight, rounded caps, no decorative icon fills.
- **Central tokens:** use the documented palette instead of introducing one-off colors.
- **Editable sources:** keep SVG source files in the repository and use Figma for visual editing.
- **No project gallery:** the system deliberately excludes project cards, showcase grids, and featured repositories.

See [DESIGN-GUIDE.md](DESIGN-GUIDE.md) for specifications and [CUSTOMIZATION-CHECKLIST.md](CUSTOMIZATION-CHECKLIST.md) for the publishing workflow.
