# Design guide

## Intent

This is a roadmap-first profile identity for a developing software engineer with a product-design mindset. The story moves from fundamentals to shipping thoughtful products. The visual system should feel focused, approachable, and technical without looking like a product dashboard.

## Color tokens

Source of truth: [`assets/design-tokens.css`](assets/design-tokens.css). The SVG files repeat concrete hex values so they remain portable when opened directly in Figma; keep those values in sync when changing the palette.

| Token | Value | Use |
| --- | --- | --- |
| `--color-canvas` | `#0B0F14` | Deep charcoal page background |
| `--color-surface` | `#111821` | Raised panel/background |
| `--color-surface-soft` | `#151F2B` | Subtle inner emphasis |
| `--color-blue` | `#3B82F6` | Electric blue primary accent |
| `--color-blue-bright` | `#60A5FA` | Highlight and active marker |
| `--color-blue-muted` | `#1D4ED8` | Secondary blue/depth |
| `--color-text` | `#F3F6FA` | Main text |
| `--color-text-muted` | `#A5B1C2` | Supporting text |
| `--color-line` | `#2A3543` | Borders and inactive roadmap line |
| `--color-success` | `#34D399` | Optional completed marker |

Avoid adding more accent hues unless they communicate a distinct state. Maintain strong text contrast and check contrast after making color changes.

## Type and layout

- Use a clean sans-serif such as Inter, system UI, or GitHub's native sans-serif.
- Hero headline: 28–36 px in a wide banner; supporting copy: 14–16 px.
- Section titles: 18–22 px; roadmap labels: 14–16 px; captions: 12–14 px.
- Leave generous vertical space between identity, roadmap, and contact details.
- Keep body copy short. A profile README is a scan-first landing page, not a resume.
- For responsive exports, keep the roadmap readable at mobile widths; stack stages if needed.

## Icon and illustration rules

- Minimal outline icons, 1.75–2 px stroke, rounded joins and caps.
- Use simple, recognizable shapes. Avoid emoji, shaded 3D icons, and mixed icon families.
- SVG source uses named groups and visible labels. Preserve these groups when editing.
- Keep purely decorative marks subordinate to the learning path.

## Roadmap narrative

Keep this exact progression unless the learning plan changes:

1. **Foundations** — programming fundamentals, problem solving, and core concepts.
2. **Software engineering** — maintainable code, architecture, collaboration, and testing.
3. **Production systems** — deployment, reliability, observability, and operating real software.
4. **AI engineering** — building useful AI-powered systems with sound engineering practice.
5. **Product building** — turning user needs into complete, polished products.

The active stage may move as learning progresses. Highlight it with electric blue; completed stages can use the optional green token sparingly; future stages use muted text and line color.

## Figma-first workflow

1. Import `assets/hero.svg`, `assets/roadmap.svg`, and `assets/divider.svg` into a Figma page named **README artwork**.
2. Create Figma color styles from the token table. Name styles exactly after the CSS token without the `--`, for example `color/blue`.
3. Preserve SVG layer/group names (`background`, `identity`, `roadmap`, `divider`, and `icon-*`) where possible.
4. Edit layout and typography in Figma. Keep text as text until the final export to preserve editability.
5. Export SVG with text preserved when supported; otherwise outline text only in the export copy and keep the source editable.
6. Commit source SVGs and any updated tokens together. Preview the result in GitHub's README renderer.

## GitHub README constraints

- GitHub Markdown supports headings, lists, links, and embedded images; it does not run custom CSS.
- CSS tokens document the system but are not applied to README Markdown. SVG files use explicit fills/strokes for reliable display.
- Use repository-relative image paths once assets live in the profile repository.
- Keep alternative text meaningful. If text in an image duplicates nearby text, use concise alt text describing the graphic.
- Avoid relying on animation or external asset hosts for the core design.

## Customization points

1. Replace the sample identity and profile links in `docs/README-EXAMPLE.md`.
2. Change copy in `assets/hero.svg` and keep headline short enough for the banner.
3. Add/remove roadmap details while preserving the five-stage narrative and readable order.
4. Change tokens in the CSS file and in the SVGs/Figma styles as one coordinated edit.
5. Adjust SVG `viewBox` and dimensions only when the composition requires it; preserve a `viewBox` for scaling.
6. Export optimized copies if needed, but retain the authored SVG sources.

## Accessibility and quality

- Use visible text labels for all roadmap stages; do not communicate progress by color alone.
- Give embedded images descriptive alt text.
- Check contrast and legibility at typical GitHub desktop and mobile widths.
- Remove placeholder links and any personal data you do not want public.
