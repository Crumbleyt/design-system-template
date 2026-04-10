# One Group UI — Architecture

## 3-Layer Stack

This library uses a layered architecture. Every component passes through three layers:

```
Layer 1: Component Engine (shadcn/ui)
  Radix UI primitives + Tailwind CSS + class-variance-authority
  Provides: accessibility, keyboard navigation, focus management,
  screen readers, ARIA attributes, component variants
  You never touch this layer directly.
         |
         v
Layer 2: Samsung One UI Styling
  CSS variables: rounded corners (1rem), spacious layout,
  Samsung color palette, Inter font, iOS-inspired spacing
  Provides: the visual look — large rounded cards, circular
  avatars, panel-style sidebars, Samsung Blue accents
  This is the STRUCTURAL foundation.
         |
         v
Layer 3: One Group Brand Overlay (DESIGN.md)
  CSS variables: One Group Red (#762224), Warm Cream canvas
  (#f5f3ed), Anthropic fonts, brand-specific error colors
  Provides: company branding on top of Samsung structure
  This is the FINAL SKIN applied to every project.
         |
         v
Output: One Group UI Component
  Samsung structure + One Group branding + full accessibility
```

## Why This Architecture?

- **Layer 1 (shadcn/ui)** handles the hard stuff: accessibility, keyboard nav, focus trapping, screen reader support, ARIA roles. Building this from scratch would take months.
- **Layer 2 (Samsung One UI)** gives every component the Samsung look: large `1rem` border-radius, spacious padding, clean card layouts, sidebar panels.
- **Layer 3 (One Group)** makes it ours: our red, our fonts, our cream canvas. Swap this layer and the same components become Samsung Blue again.

## Available Themes

| Theme | `data-theme` | Purpose |
|-------|-------------|---------|
| Samsung One UI | `samsung-one-ui` | Raw Samsung styling (Samsung Blue, Inter font) |
| One Group | `one-group` | Brand overlay (One Group Red, Anthropic fonts) — **DEFAULT** |

Switch themes via environment variable:
```bash
NEXT_PUBLIC_THEME=one-group npx next dev      # One Group branded (default)
NEXT_PUBLIC_THEME=samsung-one-ui npx next dev  # Raw Samsung look
```

## Component Library (54 components)

All components live in `src/components/ui/`. They are shadcn/ui components styled with Samsung One UI structural properties.

### Core Input Components
| Component | File | Description |
|-----------|------|-------------|
| Button | `button.tsx` | Primary, secondary, outline, ghost, destructive, link variants |
| Button Group | `button-group.tsx` | Joined button sets (Samsung-style) |
| Checkbox | `checkbox.tsx` | Check/uncheck with label |
| Input | `input.tsx` | Text input field |
| Input Group | `input-group.tsx` | Input with prefix/suffix icons |
| Input OTP | `input-otp.tsx` | One-time password input |
| Label | `label.tsx` | Form field labels |
| Native Select | `native-select.tsx` | Browser-native select dropdown |
| Radio Group | `radio-group.tsx` | Radio button sets |
| Select | `select.tsx` | Custom styled select dropdown |
| Slider | `slider.tsx` | Range slider |
| Switch | `switch.tsx` | Toggle switch (Samsung-style) |
| Textarea | `textarea.tsx` | Multi-line text input |
| Toggle | `toggle.tsx` | Toggle button |
| Toggle Group | `toggle-group.tsx` | Grouped toggles |

### Layout & Container Components
| Component | File | Description |
|-----------|------|-------------|
| Accordion | `accordion.tsx` | Expandable/collapsible sections |
| Card | `card.tsx` | Content container with Samsung rounded corners |
| Collapsible | `collapsible.tsx` | Show/hide content |
| Dialog | `dialog.tsx` | Modal dialog |
| Drawer | `drawer.tsx` | Slide-out panel (Samsung-style bottom sheet) |
| Popover | `popover.tsx` | Floating content panel |
| Resizable | `resizable.tsx` | Resizable split panels |
| Scroll Area | `scroll-area.tsx` | Custom scrollbar container |
| Separator | `separator.tsx` | Visual divider |
| Sheet | `sheet.tsx` | Slide-out side panel |
| Sidebar | `sidebar.tsx` | Navigation sidebar (Samsung-style circular panels) |

### Navigation Components
| Component | File | Description |
|-----------|------|-------------|
| Breadcrumb | `breadcrumb.tsx` | Path navigation |
| Command | `command.tsx` | Command palette (Cmd+K) |
| Context Menu | `context-menu.tsx` | Right-click menu |
| Dropdown Menu | `dropdown-menu.tsx` | Dropdown menu |
| Menubar | `menubar.tsx` | Top menu bar |
| Navigation Menu | `navigation-menu.tsx` | Primary navigation |
| Pagination | `pagination.tsx` | Page navigation |
| Tabs | `tabs.tsx` | Tab navigation |

### Data Display Components
| Component | File | Description |
|-----------|------|-------------|
| Alert | `alert.tsx` | Informational alert banner |
| Alert Dialog | `alert-dialog.tsx` | Confirmation dialog |
| Avatar | `avatar.tsx` | User avatar (Samsung circular style) |
| Badge | `badge.tsx` | Status badge |
| Calendar | `calendar.tsx` | Date picker calendar |
| Carousel | `carousel.tsx` | Image/content carousel |
| Chart | `chart.tsx` | Data visualization (Recharts) |
| Hover Card | `hover-card.tsx` | Hover-triggered info card |
| Progress | `progress.tsx` | Progress bar |
| Skeleton | `skeleton.tsx` | Loading placeholder |
| Spinner | `spinner.tsx` | Loading spinner |
| Table | `table.tsx` | Data table |
| Tooltip | `tooltip.tsx` | Hover tooltip |

### Utility Components
| Component | File | Description |
|-----------|------|-------------|
| Aspect Ratio | `aspect-ratio.tsx` | Fixed aspect ratio container |
| Combobox | `combobox.tsx` | Searchable select |
| Direction | `direction.tsx` | RTL/LTR direction control |
| Empty | `empty.tsx` | Empty state placeholder |
| Field | `field.tsx` | Form field wrapper |
| Item | `item.tsx` | List item |
| Kbd | `kbd.tsx` | Keyboard shortcut display |
| Sonner | `sonner.tsx` | Toast notifications |

## Samsung One UI Properties Enforced

These Samsung design properties are built into every component via the `--radius: 1rem` token and component CSS:

- **Large rounded corners** (1rem base radius) — Samsung's signature
- **Spacious padding** — more generous than typical web components
- **Circular avatars** — Samsung-style user icons
- **Panel-style sidebars** — rounded card-based navigation
- **Bottom sheet drawers** — Samsung-style slide-up panels
- **Button groups** — joined button sets with shared border radius
- **Clean card layouts** — white cards on light gray background
- **iOS-inspired toggle switches** — Samsung One UI toggle style

## Responsive Design

All components are responsive by default via Tailwind CSS breakpoints:

| Breakpoint | Width | CSS Class Prefix |
|-----------|-------|-----------------|
| Mobile | <640px | `sm:` |
| Tablet | 640-768px | `md:` |
| Desktop | 768-1024px | `lg:` |
| Wide | 1024-1280px | `xl:` |
| Ultra Wide | 1280px+ | `2xl:` |

The Samsung One UI layout adapts automatically:
- **Mobile:** Full-width cards, stacked layout, bottom sheet navigation
- **Tablet:** 2-column grids, sidebar collapses to sheet
- **Desktop:** Full sidebar, multi-column layouts, hover interactions

## Font Licensing

Anthropic Serif, Anthropic Sans, and Anthropic Mono fonts in `/public/fonts/anthropic/` are **INTERNAL USE ONLY**.

For public-facing products, the system automatically falls back to:
- Georgia (serif headlines)
- Inter (body/UI)
- JetBrains Mono (code)

See `DESIGN.md` > `design/03-typography.md` for full details.

## File Structure

```
one-group-ui/
  ARCHITECTURE.md          ← You are here
  DESIGN.md                ← Brand overlay index (points to design/ sections)
  design/                  ← 8 indexed brand guide sections
    01-brand-overview.md
    02-color-palette.md
    03-typography.md
    04-components.md
    05-layout-spacing.md
    06-ai-token-map.md
    07-css-variables.md
    08-rules.md
  src/
    app/
      globals.css           ← All theme CSS variables (Samsung + One Group)
      layout.tsx            ← Root layout with font loading + theme activation
    components/
      ui/                   ← 54 UI components (shadcn/ui + Samsung styling)
      theme-provider.tsx    ← Dark/light mode provider
      theme-switcher.tsx    ← Theme toggle UI
    config/
      theme.ts              ← Theme selection (samsung-one-ui | one-group)
    lib/
      utils.ts              ← Tailwind merge utility (cn function)
  public/
    fonts/anthropic/        ← 6 Anthropic font files (WOFF2)
    images/                 ← Logo and brand assets
```
