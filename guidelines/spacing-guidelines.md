# Spacing

## 1. Overview

- **What it is:** Spacing is a systematic approach to creating consistent vertical and horizontal space between elements. All components follow a 4px spacing system, which serves as our memorable base number to build upon in order to establish spatial values that are utilised by every component. By following a set spatial convention, we decrease design complexity while increasing consistency across the application.

- **When to use:**
  - To create visual hierarchy and structure between components
  - To establish consistent vertical rhythms throughout the interface
  - To define negative space and structure within components
  - To separate interactive elements and ensure proper touch targets
  - To align elements to a baseline grid for consistent layout
  - To create breathing room and improve readability

- **When not to use:**
  - Don't use multiple spacers to define space (use a single appropriate spacer)
  - Don't allow spacers to overlap content
  - Don't allow components to misalign within the space
  - Don't create custom spacing values outside the 4px system
  - Don't use spacing inconsistently across similar components

- **Accessibility note:** Proper spacing ensures touch targets meet minimum size requirements (48px minimum). Maintain at least 8px space between touch targets to prevent accidental interactions. The 4px baseline grid supports consistent alignment and structure, which aids users with visual impairments in understanding page layout.

## 2. Design Tokens

Our spacing system is built upon a 4px baseline grid. The structure of our pages is created through a percentage-based grid system that determines the position of components and how they expand. The grid takes the form of 12-columns on desktop and 8-columns for mobile.

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Pixel size | Role / notes |
|------------|--------------------|------------|--------------|
| Semantic   | `{semantic.spacing.lounge}` | 4px | Smallest spacing unit, base of the system |
| Semantic   | `{semantic.spacing.club}` | 8px | Tight spacing for closely related elements |
| Semantic   | `{semantic.spacing.hall}` | 12px | Standard spacing for component groups |
| Semantic   | `{semantic.spacing.auditorium}` | 16px | Comfortable spacing for sections |
| Semantic   | `{semantic.spacing.theatre}` | 20px | Medium spacing for distinct sections |
| Semantic   | `{semantic.spacing.amphitheatre}` | 24px | Larger spacing for major sections |
| Semantic   | `{semantic.spacing.arena}` | 32px | Significant spacing for page sections |
| Semantic   | `{semantic.spacing.stadium}` | 48px | Large spacing for major page divisions |
| Semantic   | `{semantic.spacing.dome}` | 64px | Extra large spacing for hero sections |
| Semantic   | `{semantic.spacing.field}` | 88px | Maximum spacing for major page breaks |

**White-labelling note:** Spacing tokens use semantic naming (venue names) that remain consistent across brands. The pixel values are fixed and should not be modified per brand, as they form the foundation of the 4px baseline grid system. This ensures consistent spacing hierarchy and alignment across all brand implementations.

## 3. Usage Guidelines

### Horizontal Spacing

The spacers we use determine both horizontal space as well as vertical space. Spacing tokens can be applied in any direction to create consistent spacing between elements.

### Vertical Spacing

Our vertical spaces act as building blocks that hold components apart. Stack them to create bigger spaces, keeping everything to multiples of 4px. Use vertical spaces to support hierarchies and create vertical rhythms.

### Inside, Outside and Alignment

Use spacers to create and define negative space. They can also be used inside components to create consistent internal structure. Spacers define both space between components and negative space within components.

### ✅ Do:

- Use the 4px baseline grid for all spacing decisions
- Stack spacing tokens to create larger spaces (e.g., 4px + 4px = 8px)
- Use spacers to define both space between components and negative space within components
- Align all elements to the 4px baseline grid
- Use appropriate spacing tokens for the hierarchy level needed
- Maintain consistent spacing across similar component types
- Use spacers inside components to create consistent internal structure

### ❌ Don't:

- Don't use multiple spacers to define space (use a single appropriate spacer)
- Don't allow spacers to overlap content
- Don't allow components to misalign within the space
- Don't create custom spacing values outside the defined system
- Don't use spacing inconsistently across similar components
- Don't break the 4px baseline grid alignment

## 4. Responsive Behaviour

### Grid System

The grid is made up of three parts: margins, gutters, and columns. Our margins have set values whereas our columns and gutters are fluid and automatically adjust depending on the screen width.

| Breakpoint | Container width | Columns | Margin width | Gutter width |
|-----------|-----------------|---------|--------------|--------------|
| Desktop   | Fluid           | 12      | 96px         | Fluid        |
| Mobile    | Fluid           | 8       | 16px         | Fluid        |

### Grid Flexibility

Due to the nature of our grid being percentage-based, we have far more flexibility in how it can be used. Components can span:
- 100% (full width)
- 50% (half width)
- 33.3% (one-third width)
- 25% (quarter width)
- 20% (one-fifth width)
- 12.5% (one-eighth width)
- 66.6% (two-thirds width)
- 75% (three-quarters width)
- And various combinations thereof

The grid can contain either 1, 2, 3, or 4 components horizontally on desktop, and adapts accordingly on mobile.

### Spacing Consistency

Spacing values remain consistent across all breakpoints. The 4px baseline grid applies universally, ensuring consistent vertical rhythms and alignment regardless of screen size.

## 5. Accessibility (A11y)

### Touch Targets

- **Minimum hit area:** Touch targets must have a minimum hit area of 48px × 48px
- **Touch target margins:** Maintain a minimum of 8px space between touch targets to prevent accidental interactions
- **Visual vs. hit area:** The visual element can be smaller than 48px, but the interactive hit area must meet the minimum requirement

### Visual Hierarchy

- Proper spacing creates clear visual hierarchy, helping users understand content relationships
- Consistent spacing supports cognitive accessibility by creating predictable patterns
- The 4px baseline grid ensures consistent alignment, which aids users with visual impairments

### Keyboard Navigation

- Ensure sufficient spacing between interactive elements for keyboard navigation
- Spacing should not interfere with focus indicators
- Maintain clear separation between focusable elements

## 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 2.0     | 2025-01-15 | Spacing 2.0 guidelines. Updated version number. | ✅ Current version |
| 1.0     | Legacy     | Initial spacing guidelines extracted from Figma. 4px baseline grid system with venue-named spacing tokens. | ⚠️ Deprecated |

---

**Status:** 🟢 Complete and in-sync with code  
**Last updated:** 15th January, 2025

