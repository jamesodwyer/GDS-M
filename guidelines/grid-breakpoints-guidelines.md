# Grid & Breakpoints

### 1. Overview

- **What it is:** A structured column-based grid designed for consistency and scalability across breakpoints. This grid ensures predictable layouts, making it easier to maintain visual hierarchy and alignment in both design and development.

- **When to use:**
  - Creating layouts for Ticketmaster products
  - Positioning components consistently across screen sizes
  - Ensuring alignment with development partners
  - Designing responsive experiences

- **When not to use:**
  - TODO: Add anti-patterns from Figma file.

- **Accessibility note:** TODO: Add accessibility guidance related to grid and layout from Figma file.

### 2. Grid System

The grid system provides a structured column-based layout designed for consistency and scalability across breakpoints. It covers column counts, margin widths, and gutter widths for each breakpoint, enabling predictable layouts for both design and development.

### 3. Usage Guidelines

- **✅ Do:**
  - Create focused layouts for at least three primary screen sizes: small (375px), medium (744px), and large (1440px)
  - Design mobile-first (starting from 320px)
  - Scale gracefully up to 1680px+
  - Use 100% width for full-width components
  - Use specific column widths when components need constrained sizing
  - Test layouts at 320px minimum supported viewport
  - Design across the full range of supported screen sizes to validate behaviour at all breakpoints

- **❌ Don't:**
  - TODO: Add key "misuse" points from Figma file.

### 4. Responsive Behaviour

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Small (320-512px) | 4 columns flexed, 16px gutters, 16px margins fixed | iPhone 13 mini frame |
| Medium (512–1024px) | 8 columns flexed, 16px gutters, 32px margins fixed | iPad mini 8.3 frame |
| Large (1024–1680px) | 12 columns flexed, 32px gutters, 64px margins fixed | Desktop/Wireframe |
| XLarge (1680+px) | 12 columns flexed until max width, 32px gutters, 96px margins fixed. Max width of container 1920px, margins become auto | MacBook Pro 16" |

**Screen sizes for design reference:**
- Small: 375px (design reference), supports down to 320px (minimum supported viewport)
- Medium: 744px (iPad mini 8.3 in Figma frames)
- Large: 1440px (Desktop in Figma frames)
- XLarge: 1728px (Desktop in Figma frames)

**Breakpoints for development:**
- Small: 512px
- Medium: 1024px
- Large: 1680px

**Note:** While 320px is not a standard design size, it is our minimum supported viewport and should always be considered when testing and reviewing layouts.

### 5. Accessibility (A11y)

- TODO: Add explicit accessibility contrast rules for Grid system.
- TODO: Add focus, outline, and layout accessibility guidance.


### 7. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.1     | 2025-01-15 | Removed design-system value tables; to be re-added later. | ✅ Current version |
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ⚠️ Deprecated |

