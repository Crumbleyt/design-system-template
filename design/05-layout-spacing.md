# 5. Layout & Spacing

[Back to Index](../DESIGN.md)

## Spacing System

- Base unit: 8px
- Scale: 3px, 4px, 6px, 8px, 10px, 12px, 16px, 20px, 24px, 30px
- Button padding: asymmetric (0px 12px 0px 8px) or balanced (8px 16px)
- Card internal padding: 24-32px
- Section vertical spacing: 80-120px between major sections
- Max container: ~1200px centered

## Border Radius Scale

| Name | Size | Use |
|------|------|-----|
| Sharp | 4px | Minimal inline elements |
| Subtly rounded | 6-7.5px | Small buttons, secondary elements |
| Comfortably rounded | 8-8.5px | Standard buttons, cards, containers |
| Generously rounded | 12px | Primary buttons, inputs, nav |
| Very rounded | 16px | Featured containers, video players |
| Highly rounded | 24px | Tag-like elements |
| Maximum rounded | 32px | Hero containers, embedded media |

## Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (0) | No shadow, no border | Canvas background, inline text |
| Contained (1) | `1px solid #f0eee6` (light) or `1px solid #323234` (dark) | Standard cards, sections |
| Ring (2) | `0px 0px 0px 1px` ring shadows using warm grays | Interactive cards, buttons, hover |
| Whisper (3) | `rgba(0,0,0,0.05) 0px 4px 24px` | Elevated cards, screenshots |
| Inset (4) | `inset 0px 0px 0px 1px` at 15% opacity | Active/pressed states |

## Responsive Breakpoints

| Breakpoint | Width | Key Changes |
|-----------|-------|-------------|
| Small Mobile | <479px | Stacked, compact typography |
| Mobile | 479-640px | Single column, hamburger nav |
| Large Mobile | 640-767px | Slightly wider content area |
| Tablet | 768-991px | 2-column grids begin |
| Desktop | 992px+ | Full multi-column layout, 64px hero type |
