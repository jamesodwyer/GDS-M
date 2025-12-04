# Foundations Guidelines

## Colour

### 1. Overview

- **What it is:** TODO: Add description of the colour system from Figma file.

- **When to use:** TODO: Add usage scenarios from Figma file.

- **When not to use:** TODO: Add anti-patterns from Figma file.

- **Accessibility note:** TODO: Add WCAG contrast requirements and accessibility guidance from Figma file.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | TODO | TODO | Base raw value |
| Brand      | TODO | ↦ Core token | Brand mapping |
| Semantic   | TODO | ↦ Brand token | Contextual meaning |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** TODO: Explain how colour tokens support white-labelling across brands.

### 3. Usage Guidelines

- **✅ Do:**
  - TODO: Add key "good usage" points from Figma file.

- **❌ Don't:**
  - TODO: Add key "misuse" points from Figma file.

### 4. Responsive Behaviour (if applicable)

TODO: Add responsive colour behaviour if applicable.

### 5. Accessibility (A11y)

- TODO: Add WCAG 2.1/2.2 AA colour contrast rules.
- TODO: Add focus, outline, and high-contrast palette guidance.
- TODO: Add tokens specifically used for accessibility.

### 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

---

## Typography

### 1. Overview

- **What it is:** TODO: Add description of the typography system from Figma file.

- **When to use:** TODO: Add usage scenarios from Figma file.

- **When not to use:** TODO: Add anti-patterns from Figma file.

- **Accessibility note:** TODO: Add minimum readable text sizes, line height, and motion guidance from Figma file.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | TODO | TODO | Base raw value |
| Brand      | TODO | ↦ Core token | Brand mapping |
| Semantic   | TODO | ↦ Brand token | Contextual meaning |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** TODO: Explain how typography tokens support white-labelling across brands.

### 3. Usage Guidelines

- **✅ Do:**
  - TODO: Add key "good usage" points from Figma file.

- **❌ Don't:**
  - TODO: Add key "misuse" points from Figma file.

### 4. Responsive Behaviour

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Small     | TODO | TODO |
| Medium    | TODO | TODO |
| Large     | TODO | TODO |

### 5. Accessibility (A11y)

- TODO: Add WCAG 2.1/2.2 AA readable text size requirements.
- TODO: Add line height and spacing guidance.
- TODO: Add motion and animation guidance for typography.
- TODO: Add tokens specifically used for accessibility.

### 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

---

## Spacing

### 1. Overview

- **What it is:** TODO: Add description of the spacing system from Figma file.

- **When to use:** TODO: Add usage scenarios from Figma file.

- **When not to use:** TODO: Add anti-patterns from Figma file.

- **Accessibility note:** TODO: Add minimum spacing for touch targets and accessibility guidance from Figma file.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | TODO | TODO | Base raw value |
| Brand      | TODO | ↦ Core token | Brand mapping |
| Semantic   | TODO | ↦ Brand token | Contextual meaning |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** TODO: Explain how spacing tokens support white-labelling across brands.

### 3. Usage Guidelines

- **✅ Do:**
  - TODO: Add key "good usage" points from Figma file.

- **❌ Don't:**
  - TODO: Add key "misuse" points from Figma file.

### 4. Responsive Behaviour (if applicable)

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Small     | TODO | TODO |
| Medium    | TODO | TODO |
| Large     | TODO | TODO |

### 5. Accessibility (A11y)

- TODO: Add minimum tap target size requirements (WCAG 2.1/2.2 AA).
- TODO: Add spacing guidance for focus indicators.
- TODO: Add tokens specifically used for accessibility.

### 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

---

## Grid & Breakpoints

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

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | TODO | TODO | Base raw value |
| Brand      | TODO | ↦ Core token | Brand mapping |
| Semantic   | `{semantic.breakpoint.sm}` | `"512px"` | Small breakpoint |
| Semantic   | `{semantic.breakpoint.md}` | `"1024px"` | Medium breakpoint |
| Semantic   | `{semantic.breakpoint.lg}` | `"1680px"` | Large breakpoint |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** Grid tokens support white-labelling by allowing brand-specific margin and gutter adjustments while maintaining consistent column structures across breakpoints.

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

- TODO: Add explicit accessibility contrast rules for Grid tokens.
- TODO: Add focus, outline, and layout accessibility guidance.

### 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

---

## Elevation

### 1. Overview

- **What it is:** TODO: Add description of the elevation/shadow system from Figma file.

- **When to use:** TODO: Add usage scenarios from Figma file.

- **When not to use:** TODO: Add anti-patterns from Figma file.

- **Accessibility note:** TODO: Add accessibility guidance for elevation, shadows, and visual hierarchy from Figma file.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | TODO | TODO | Base raw value |
| Brand      | TODO | ↦ Core token | Brand mapping |
| Semantic   | TODO | ↦ Brand token | Contextual meaning |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** TODO: Explain how elevation tokens support white-labelling across brands.

### 3. Usage Guidelines

- **✅ Do:**
  - TODO: Add key "good usage" points from Figma file.

- **❌ Don't:**
  - TODO: Add key "misuse" points from Figma file.

### 4. Responsive Behaviour (if applicable)

TODO: Add responsive elevation behaviour if applicable.

### 5. Accessibility (A11y)

- TODO: Add explicit accessibility contrast rules for Elevation tokens.
- TODO: Add focus, outline, and visual hierarchy guidance.
- TODO: Add tokens specifically used for accessibility.

### 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

