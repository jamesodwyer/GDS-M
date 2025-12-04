# Spacing

### 1. Overview

- **What it is:** Spacing creates clarity, rhythm, and structure. It helps users scan content, navigate interfaces easily, and interact comfortably across all devices. Consistent spacing improves accessibility and reduces cognitive load.

- **When to use:**
  - Creating layouts for Ticketmaster products
  - Positioning components consistently across screen sizes
  - Maintaining visual hierarchy and content structure
  - Ensuring clear separation between interactive elements
  - Applying padding within components and margins between components

- **When not to use:**
  - Hardcoding pixel values instead of using tokens
  - Stacking multiple small spacings to mimic large gaps
  - Reducing spacing between interactive elements below 8px

- **Accessibility note:** Consistent spacing improves accessibility by reducing cognitive load and ensuring clear separation between interactive elements. Minimum spacing of 8px should be maintained between interactive elements.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Core       | `$spacing-01` | `2px` | Base raw value |
| Core       | `$spacing-02` | `4px` | Base raw value |
| Core       | `$spacing-03` | `8px` | Base raw value |
| Core       | `$spacing-04` | `12px` | Base raw value |
| Core       | `$spacing-05` | `16px` | Base raw value |
| Core       | `$spacing-06` | `20px` | Base raw value |
| Core       | `$spacing-07` | `24px` | Base raw value |
| Core       | `$spacing-08` | `32px` | Base raw value |
| Core       | `$spacing-09` | `40px` | Base raw value |
| Core       | `$spacing-10` | `48px` | Base raw value |
| Core       | `$spacing-11` | `56px` | Base raw value |
| Core       | `$spacing-12` | `64px` | Base raw value |
| Core       | `$spacing-13` | `72px`, `80px`, `96px`, `112px`, `128px` | Base raw value |
| Semantic   | `stack.form` | Desktop: `24px` (`core.dimension.600`), Mobile: `20px` (`core.dimension.500`) | Form stack spacing |
| Semantic   | `layout.content-to-button` | Desktop: `32px` (`core.dimension.800`), Mobile: `24px` (`core.dimension.600`) | Content to button spacing |
| Semantic   | `layout.between-sections` | `96px` | Spacing between sections |
| Semantic   | `layout.heading-spacer` | `32px` | Margins below a heading |
| Semantic   | `layout.title-spacer` | `24px` | Margins below a title |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**White-labelling note:** Spacing tokens support white-labelling by allowing brand-specific spacing adjustments while maintaining consistent scale and rhythm. Form stack spacing, for example, can be adjusted per brand while maintaining the overall spacing system structure.

### 3. Usage Guidelines

- **✅ Do:**
  - Use spacing tokens throughout components and layouts
  - Match spacing choices to content hierarchy and layout scale
  - Stick to the predefined scale — if a new size is needed, discuss it with the system team
  - Use smaller spacing tokens for component padding and content alignment
  - Use larger tokens for layout gaps and page-level breathing space
  - Apply spacing using tokens — never fixed values — to ensure consistency, responsiveness, and adaptability across themes or brands
  - Use the Stack component for managing spacing between elements in both horizontal and vertical orientations

- **❌ Don't:**
  - Hardcode pixel values
  - Stack multiple small spacings to mimic large gaps
  - Reduce spacing between interactive elements below 8px
  - Use arbitrary spacing values without semantic meaning

### 4. Responsive Behaviour

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Desktop | Larger spacing values for breathing room | `stack.form` = 24px, `layout.content-to-button` = 32px |
| Mobile | Smaller spacing values for compact layouts | `stack.form` = 20px, `layout.content-to-button` = 24px |

**Spacing Scale:**
- **2–24px:** Increments of 4px (ideal for fine-tuned spacing)
- **24–80px:** Increments of 8px
- **80px+:** Increments of 16px (supports macro-level layout structuring)

**Scale values:** 2, 4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64, 72, 80, 96, 112, 128

**Note:** The scale is based on a base of 8px to maintain consistency with our grid system and elevation rhythm.

### 5. Accessibility (A11y)

- Maintain minimum spacing of 8px between interactive elements to ensure clear separation and reduce accidental interactions
- Use consistent spacing to reduce cognitive load and improve content scannability
- Ensure spacing supports clear visual hierarchy for screen reader users
- Apply semantic spacing tokens that align with content structure and component relationships

### 6. Applying Spacing

**Layout:**
- **Grid Margins & Gutters** – Defines spacing between columns in the grid and the edge of the page
- **Margins & Padding** – Controls spacing between sections and containers

**Components:**
- **Padding** – Internal spacing within buttons, cards, modals, and other UI elements
- **Margins** – External spacing between components to maintain clear separation

**Stacking:**
- Stack is a spacing method that ensures equal distance between components or groups of items
- The Stack component provides a flexible way to manage spacing using the Ticketmaster spacing scale
- Defines appropriate gaps between elements in both horizontal and vertical orientations
- Eliminates the need for individual components to define margins, instead delegating spacing and positioning to their parent containers
- Supports a custom gap property, allowing users to specify a precise spacing value for greater layout flexibility

**Form Stacks:**
- Forms have one clear defined spacer for layouts
- Can use a Design Token to govern this value
- Can be changed when branding other white-labels to provide flexibility

**Semantic Spacing:**
- Semantic spacing ensures that spacing values are applied with meaningful intent
- Aligns with content structure, component relationships, and hierarchy
- Instead of using arbitrary spacing values, semantic spacing assigns names to spacing tokens based on their purpose
- Improves consistency and maintainability across Ticketmaster products

### 7. Update Me

**⚠️ Token Values:** The token names and values in section 2 (Design Tokens) are placeholders extracted from the Figma file. These should be replaced with the actual token names and values from your design token system before finalising this document. Please verify:
- Core token naming convention matches your system
- Semantic token names are correct
- Token values (pixel values) are accurate
- All token mappings are properly documented

### 8. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

