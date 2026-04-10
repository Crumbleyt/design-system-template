# 6. AI Conversion Token Map

[Back to Index](../DESIGN.md)

> **For AI converters only.** Read this when converting Stitch/design tool exports. Every skin class gets a deterministic mapping. Layout classes pass through untouched.

## Skin Class Replacements

| Stitch / Source Class | One Group Token | CSS Variable | Resolved Value |
|----------------------|-----------------|-------------|----------------|
| `bg-blue-*`, `bg-indigo-*`, `bg-primary-*` | `bg-primary` | `--primary` | `#762224` |
| `bg-gray-50`, `bg-gray-100`, `bg-slate-50` | `bg-background` | `--background` | `#f5f3ed` |
| `bg-white` | `bg-card` | `--card` | `#ffffff` |
| `bg-gray-800`, `bg-gray-900`, `bg-slate-800` | `bg-card` (dark) | `--card` | `#323234` |
| `bg-gray-200`, `bg-slate-200` | `bg-secondary` | `--secondary` | `#e8e6dc` |
| `bg-gray-100`, `bg-slate-100` | `bg-muted` | `--muted` | `#f0eee6` |
| `bg-red-50`, `bg-red-100` | `bg-destructive/10` | `--destructive` | `#d4453a` |
| `text-gray-900`, `text-slate-900`, `text-black` | `text-foreground` | `--foreground` | `#141413` |
| `text-gray-600`, `text-slate-600` | `text-muted-foreground` | `--muted-foreground` | `#5e5d59` |
| `text-gray-400`, `text-gray-500`, `text-slate-400` | `text-muted-foreground` | `--muted-foreground` | `#87867f` |
| `text-blue-*`, `text-primary-*` | `text-primary` | `--primary` | `#762224` |
| `text-red-*`, `text-error-*` | `text-destructive` | `--destructive` | `#d4453a` |
| `text-white` (on dark) | `text-foreground` | `--foreground` | `#fffcf8` |
| `border-gray-200`, `border-gray-300`, `border-slate-*` | `border-border` | `--border` | `#f0eee6` |
| `ring-blue-*`, `ring-primary-*` | `ring-ring` | `--ring` | `#d1cfc5` |
| `divide-gray-200` | `divide-border` | `--border` | `#f0eee6` |
| `font-sans`, `font-body` | `font-sans` | `--font-sans` | Anthropic Sans |
| `font-serif`, `font-display` | `font-heading` | `--font-heading` | Anthropic Serif |
| `font-mono` | `font-mono` | `--font-mono` | Anthropic Mono |
| `shadow-sm`, `shadow`, `shadow-md` | ring shadow | — | `0px 0px 0px 1px var(--ring)` |

## Layout Classes — Pass Through Untouched

These classes are **NEVER** modified during conversion (Strict Skin Mode):

`flex`, `grid`, `block`, `inline`, `inline-flex`, `inline-grid`, `hidden`, `p-*`, `px-*`, `py-*`, `pt-*`, `pr-*`, `pb-*`, `pl-*`, `m-*`, `mx-*`, `my-*`, `mt-*`, `mr-*`, `mb-*`, `ml-*`, `gap-*`, `gap-x-*`, `gap-y-*`, `space-x-*`, `space-y-*`, `w-*`, `h-*`, `min-w-*`, `min-h-*`, `max-w-*`, `max-h-*`, `size-*`, `top-*`, `bottom-*`, `left-*`, `right-*`, `inset-*`, `absolute`, `relative`, `fixed`, `sticky`, `static`, `z-*`, `overflow-*`, `col-span-*`, `row-span-*`, `grid-cols-*`, `grid-rows-*`, `order-*`, `justify-*`, `items-*`, `self-*`, `content-*`, `place-*`, `grow`, `shrink`, `basis-*`, `flex-row`, `flex-col`, `flex-wrap`, `flex-nowrap`, `aspect-*`, `container`, `columns-*`

## Application Order

```
1. Base theme tokens load (Samsung One UI)
2. Stitch conversion runs — AI reads this token map
3. Skin classes replaced with semantic tokens
4. Layout classes preserved verbatim
5. One Group CSS variables resolve at runtime
6. Result: branded, consistent, theme-switchable UI
```
