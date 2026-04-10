# 3. Typography

[Back to Index](../DESIGN.md)

## Font Families

| Role | Font | CSS Variable | Fallback |
|------|------|-------------|----------|
| Headlines | Anthropic Serif | `--font-heading` | Georgia, serif |
| Body / UI | Anthropic Sans | `--font-sans` | Inter, system-ui, sans-serif |
| Code | Anthropic Mono | `--font-mono` | JetBrains Mono, monospace |

**Font files location:** `/public/fonts/anthropic/` (6 WOFF2 files)

## LICENSING WARNING

> **INTERNAL USE ONLY.** Anthropic fonts are proprietary typefaces owned by Anthropic. They are sourced from Anthropic's public website for use in **internal tools only**.
>
> **For public-facing products, external docs, client portals, or any UI visible to non-employees:** Use fallback fonts (Georgia, Inter, JetBrains Mono).
>
> See ONE-GROUP-STYLE.md for full licensing details.

## Type Hierarchy

| Role | Font | Size | Weight | Line Height |
|------|------|------|--------|-------------|
| Display / Hero | Anthropic Serif | 64px (4rem) | 500 | 1.10 |
| Section Heading | Anthropic Serif | 52px (3.25rem) | 500 | 1.20 |
| Sub-heading Large | Anthropic Serif | 36px (~2.3rem) | 500 | 1.30 |
| Sub-heading | Anthropic Serif | 32px (2rem) | 500 | 1.10 |
| Sub-heading Small | Anthropic Serif | 25px (~1.6rem) | 500 | 1.20 |
| Feature Title | Anthropic Serif | 20.8px (1.3rem) | 500 | 1.20 |
| Body Serif | Anthropic Serif | 17px (1.06rem) | 400 | 1.60 |
| Body Large | Anthropic Sans | 20px (1.25rem) | 400 | 1.60 |
| Body / Nav | Anthropic Sans | 17px (1.06rem) | 400-500 | 1.00-1.60 |
| Body Standard | Anthropic Sans | 16px (1rem) | 400-500 | 1.25-1.60 |
| Body Small | Anthropic Sans | 15px (0.94rem) | 400-500 | 1.00-1.60 |
| Caption | Anthropic Sans | 14px (0.88rem) | 400 | 1.43 |
| Label | Anthropic Sans | 12px (0.75rem) | 400-500 | 1.25-1.60 |
| Overline | Anthropic Sans | 10px (0.63rem) | 400 | 1.60 |
| Code | Anthropic Mono | 15px (0.94rem) | 400 | 1.60 |

## Typography Rules

- **Serif for authority, sans for utility.** Anthropic Serif carries all headline content. Anthropic Sans handles UI text.
- **Single weight for serifs.** All Anthropic Serif headings use weight 500. No bold, no light.
- **Relaxed body line-height.** Most body text uses 1.60 — more generous than typical tech sites.
- **Tight headings.** Line-heights of 1.10-1.30 for headings — tight but not compressed.
- **Micro letter-spacing.** Small sans text (12px and below) uses 0.12px-0.5px letter-spacing.
