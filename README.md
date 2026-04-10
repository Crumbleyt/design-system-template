# One Group UI

Unified component library for One Group Developers. 54 production-ready components with Samsung One UI styling and One Group brand overlay.

## Architecture

```
shadcn/ui components (engine) → Samsung One UI (structure) → One Group brand (skin)
```

See [ARCHITECTURE.md](ARCHITECTURE.md) for full details.

## Quick Start

```bash
# Install dependencies
npm install

# Run with One Group branding (default)
npx next dev --port 3000

# Run with raw Samsung One UI look
set NEXT_PUBLIC_THEME=samsung-one-ui    # Windows CMD
$env:NEXT_PUBLIC_THEME="samsung-one-ui" # Windows PowerShell
NEXT_PUBLIC_THEME=samsung-one-ui        # macOS/Linux
npx next dev --port 3000
```

## 54 Components

**Inputs:** Button, Button Group, Checkbox, Input, Input Group, Input OTP, Label, Native Select, Radio Group, Select, Slider, Switch, Textarea, Toggle, Toggle Group

**Layout:** Accordion, Card, Collapsible, Dialog, Drawer, Popover, Resizable, Scroll Area, Separator, Sheet, Sidebar

**Navigation:** Breadcrumb, Command, Context Menu, Dropdown Menu, Menubar, Navigation Menu, Pagination, Tabs

**Data Display:** Alert, Alert Dialog, Avatar, Badge, Calendar, Carousel, Chart, Hover Card, Progress, Skeleton, Spinner, Table, Tooltip

**Utility:** Aspect Ratio, Combobox, Direction, Empty, Field, Item, Kbd, Sonner (toasts)

## Brand Guide

See [DESIGN.md](DESIGN.md) for indexed brand documentation (colors, typography, components, rules).

## License

Internal use. Anthropic fonts are not licensed for public-facing products — see [ARCHITECTURE.md](ARCHITECTURE.md#font-licensing).
