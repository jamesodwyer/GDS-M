# Elevation

### 1. Overview

- **What it is:** Elevation helps users focus on the most important elements by introducing depth and hierarchy. It clarifies relationships between surfaces and ensures interactive elements are visually prioritised.

- **When to use:**
  - Creating visual hierarchy within content
  - Establishing relationships between surfaces
  - Prioritising interactive elements
  - Creating overlays, modals, or drawers
  - Implementing sticky elements like headers or footers
  - Breaking visual rhythm with static surfaces

- **When not to use:**
  - Stacking too many elevation levels (creates clutter)
  - Using elevation alone to suggest interactivity (must pair with other cues)
  - Mixing static and inverse styling without a clear purpose

- **Accessibility note:** Always pair elevation with other cues like colour and border. Shadows alone are not enough for users who rely on high-contrast or assistive technologies.

### 2. Design Tokens

- **Token architecture reminder:**
  - Core → Brand → Semantic → Component

- **Token table:**

| Token layer | Example token name | Example value / mapping | Role / notes |
|------------|--------------------|--------------------------|-------------|
| Semantic   | `elevation.elevation-level-1` | Shadow effect | Level 1 elevation effect |
| Semantic   | `elevation.elevation-level-2` | Shadow effect | Level 2 elevation effect |
| Semantic   | `elevation.elevation-level-3` | Shadow effect | Level 3 elevation effect |
| Semantic   | `elevation.elevation-level-4` | Shadow effect | Level 4 elevation effect |
| Semantic   | `fill.elevation-level-1` | Surface fill | Level 1 surface fill |
| Semantic   | `fill.elevation-level-2` | Surface fill | Level 2 surface fill |
| Semantic   | `fill.elevation-level-3` | Surface fill | Level 3 surface fill |
| Semantic   | `fill.elevation-level-4` | Surface fill | Level 4 surface fill |
| Semantic   | `border.elevation-level-1` | Border/stroke | Level 1 border |
| Semantic   | `border.elevation-level-2` | Border/stroke | Level 2 border |
| Semantic   | `border.elevation-level-3` | Border/stroke | Level 3 border |
| Semantic   | `border.elevation-level-4` | Border/stroke | Level 4 border |
| Component  | TODO | ↦ Semantic token | Applied in UI |

**Elevation structure:** Elevation is made up of 3 properties:
- **Effects** – Shadow effects that create depth
- **Surface / Fill** – The background fill of the elevated surface
- **Border** – Border/stroke around the elevated surface (Figma calls border a stroke)

**White-labelling note:** Elevation tokens support white-labelling by allowing brand-specific shadow, fill, and border adjustments while maintaining consistent depth hierarchy across levels. The elevation system ensures visual consistency across light and dark themes.

### 3. Usage Guidelines

- **✅ Do:**
  - Use level 0 as your default canvas layer
  - Apply higher levels for overlays, sticky content, or layered hierarchies
  - Use static only to break visual rhythm, not for stacking
  - Always apply elevation using tokens — never custom shadows — to ensure visual consistency across light and dark themes
  - Pair elevation with other cues like colour and border for accessibility

- **❌ Don't:**
  - Stack too many elevation levels — it creates clutter
  - Use elevation alone to suggest interactivity
  - Mix static and inverse styling without a clear purpose
  - Create custom shadows instead of using elevation tokens

### 4. Elevation Levels

| Level | Usage | Description |
|-------|-------|-------------|
| Level 0 (Canvas) | Default | This is the default canvas level to build screens on |
| Level 1 | Content hierarchy | This level is used to provide hierarchy within content that is laid on level 0 |
| Level 2 | Sticky elements | This level is used for any sticky elements on the page such as a header or a footer |
| Level 3 | Multiple sticky elements | This level is used if there are more than one sticky elements on the page and you want to establish hierarchy between them |
| Level 4 | Overlays | This level is always used with an overlay background for elements such as modals or drawers |
| Inverse | Theme-aware | This level is dark in light mode and light in dark mode |
| Static | Visual prominence | This is agnostic of layer system and used to bring visual prominence and to break out the layout, the colour of the surface does not change between dark and light mode |

**Note:** Our elevation system includes six depth levels (0-4, plus special surfaces like Inverse and Static). These are layered consistently across the UI to establish meaning and support layout clarity.

### 5. Responsive Behaviour

Elevation levels remain consistent across breakpoints. The visual appearance of elevation (shadows, fills, borders) adapts to light and dark themes automatically through tokens.

### 6. Accessibility (A11y)

- Always pair elevation with other cues like colour and border
- Shadows alone are not enough for users who rely on high-contrast or assistive technologies
- Ensure sufficient contrast between elevated surfaces and their backgrounds
- Use elevation tokens that are designed to work with high-contrast modes
- Do not rely solely on shadow effects to indicate interactivity or hierarchy

### 7. Update Me

**⚠️ Token Values:** The token names and values in section 2 (Design Tokens) are placeholders extracted from the Figma file. These should be replaced with the actual token names and values from your design token system before finalising this document. Please verify:
- Elevation effect token names are correct (e.g., `elevation.elevation-level-1` format)
- Fill token names match your system (e.g., `fill.elevation-level-1`)
- Border/stroke token names are accurate (e.g., `border.elevation-level-1`)
- All token values (shadow effects, fill colours, border styles) are properly documented
- Token mappings work correctly in both light and dark themes

### 8. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 01/01/2025 | Initial guidelines extracted to MD. | ✅ Baseline |

