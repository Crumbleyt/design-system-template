# 1. Brand Overview

[Back to Index](../DESIGN.md)

## Visual Theme & Atmosphere

One Group's interface is a warm editorial design — unhurried, intellectual, and quietly authoritative. The experience is built on a warm cream canvas (`#f5f3ed`) that feels like quality paper rather than a digital surface. The signature brand color is a deep, corporate red (`#762224`) used sparingly for primary CTAs and brand moments. Every gray in the system carries a warm yellow-brown undertone — there are no cool blue-grays anywhere.

Typography uses the Anthropic type family: Serif for headlines (weight 500, editorial gravitas), Sans for UI and body text, Mono for code. This serif/sans split creates a literary hierarchy that says "thoughtful tool" rather than "generic dashboard."

**Key Characteristics:**
- Warm cream canvas (`#f5f3ed`) — not pure white, not cold gray
- One Group Red (`#762224`) — deep, corporate, used only for primary CTAs
- Bright Crimson accent (`#c45a5c`) — lighter red for links on dark, hover states
- Exclusively warm-toned neutrals — every gray has a yellow-brown undertone
- Ring-based shadow system (`0px 0px 0px 1px`) — border-like depth without visible borders
- Editorial serif/sans typography hierarchy

## Logo Usage

- Light surfaces: "ONE GROUP" in One Group Red `#762224`
- Dark surfaces: "ONE GROUP" in `#fffcf8`
- Logo files: SVG preferred, stored in `/public/images/`

## Available Themes

| Theme | Purpose | Default |
|-------|---------|---------|
| `samsung-one-ui` | Samsung One UI base (Inter, Samsung Blue, rounded corners) | No |
| `one-group` | One Group brand overlay (Anthropic fonts, warm cream, corporate red) | Yes |

The One Group theme is the **master overlay** — it applies final branding on top of any base theme.
