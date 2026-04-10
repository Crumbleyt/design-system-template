# 8. Rules — Do's and Don'ts

[Back to Index](../DESIGN.md)

## Do

- Use Warm Cream `#f5f3ed` as the primary light background
- Use Anthropic Serif at weight 500 for all headlines
- Use One Group Red `#762224` only for primary CTAs and brand moments
- Keep all neutrals warm-toned — every gray should have a yellow-brown undertone
- Use ring shadows (`0px 0px 0px 1px`) for interactive element states
- Use Bright Alert Red `#d4453a` for errors — never brand red
- Maintain the editorial serif/sans hierarchy
- Use generous body line-height (1.60)
- Alternate between light and dark sections for chapter-like page rhythm
- Apply generous border-radius (12-32px) for a soft, approachable feel

## Don't

- Don't use brand red `#762224` for error states — use `#d4453a`
- Don't use cool blue-grays anywhere — palette is exclusively warm-toned
- Don't use bold (700+) weight on Anthropic Serif — weight 500 is the ceiling
- Don't introduce saturated colors beyond the defined palette
- Don't use sharp corners (<6px radius) on buttons or cards
- Don't use Anthropic fonts in public-facing products (licensing)
- Don't hardcode hex values in components — always use CSS variables
- Don't modify layout classes during Strict Skin Mode conversion
- Don't use pure white (`#ffffff`) as a page background — use `#f5f3ed`
- Don't reduce body line-height below 1.40

## Master Overlay Application Order

```
1. Base theme tokens load (Samsung One UI)
2. Stitch conversion runs — AI reads design/06-ai-token-map.md
3. Skin classes replaced with semantic tokens
4. Layout classes preserved verbatim
5. One Group CSS variables resolve at runtime
6. Result: branded, consistent, theme-switchable UI
```

## Error vs Brand Color

Brand red `#762224` and error red `#d4453a` are different colors by design. Never use brand red for error states — they must be visually distinct so users don't confuse a CTA with a warning.
