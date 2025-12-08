# Elevation

## 1. Overview

- **What it is:** Elevation is the space in-between two elements on the z-axis of a view. It is a core design principle applied across all surfaces and components to establish a clear and consistent visual hierarchy. It represents the relative position of elements along the z-axis, helping users understand the structure and interactivity of the interface.

- **When to use:**
  - To establish visual hierarchy between elements
  - To indicate interactive or elevated components (cards, buttons, modals)
  - To create depth and separation between layers of content
  - To distinguish sticky elements (headers, footers) from scrollable content
  - To indicate floating panels or overlays
  - To provide visual feedback for interactive states

- **When not to use:**
  - On elements that should appear flat or integrated with the background
  - When it creates unnecessary visual noise
  - On decorative elements that don't require hierarchy indication
  - When multiple elevation levels compete for attention unnecessarily

- **Accessibility note:** Elevation helps users understand the structure and layering of the interface, which supports cognitive accessibility. Ensure sufficient contrast between elevated elements and their backgrounds. For users with motion sensitivity, consider reducing or removing elevation animations where possible.

## 2. Elevation System

Our elevation system includes three key visual elements: shadows (in this release v2.0), surface fill colour, and potentially border colour. These elements will be defined for both light and dark modes to ensure clarity and consistency across themes. Additionally, we will support inverse elevation styles in light mode for components that appear on dark backgrounds, maintaining accessibility and visual contrast.

Elevation can be represented through subtle shadows, tonal variations, or borders, depending on the context. This flexibility allows for a cohesive look and feel while supporting accessibility and clarity.

### Elevation Levels

| Level | Shadow specification | Role / notes |
|-------|---------------------|--------------|
| Level 1 | X0, Y1, Blur 4, Spread 0, Cosmos #121212 - 15% | Basic cards, alerts |
| Level 2 | X0, Y2, Blur 8, Spread 0, Cosmos #121212 - 15% | Sticky elements, headers, footers |
| Level 3 | X0, Y3, Blur 12, Spread 0, Cosmos #121212 - 18% | Multiple sticky elements, panels floating over content |
| Level 4 | X0, Y8, Blur 20, Spread 0, Cosmos #121212 - 35% | Modals, sidepanels (always used with overlay background) |

## 3. Usage Guidelines

### Elevation Levels

#### Canvas Level 0
This is the default canvas level to build screens on (Body). All content is laid on this base level.

#### Level 1
This level is used to provide hierarchy within content that is laid on level 0, i.e. basic cards, alerts.

**Examples:**
- Alert components
- Basic card elements
- Content containers that need subtle separation

#### Level 2
This level is used for any sticky elements on the page such as a header or a footer, also can be used for extra lift on cards elements. Content can then slide underneath the sticky elements.

**Examples:**
- Sticky navigation bars
- Sticky headers and footers
- Card elements requiring extra lift
- Discovery navigation with sticky category selector

#### Level 3
This level is used if there are more than one sticky elements on the page and you want to establish hierarchy between them. Also for panels floating over content.

**Examples:**
- Multiple sticky elements requiring hierarchy
- Floating panels
- Toolbars
- Seat selection tooltips
- Map zoom controls

#### Level 4
This level is always used with an overlay background for elements such as modals or sidepanels.

**Examples:**
- Modal dialogs
- Side panels
- Overlay menus
- Full-screen overlays

### ✅ Do:

- Use elevation to establish clear visual hierarchy
- Stick to a limited set of elevation levels to reduce visual noise
- Use the appropriate elevation level for the component's purpose
- Ensure elevation levels are consistent across similar components
- Use Level 4 with an overlay background for modals and sidepanels
- Use Level 2 for sticky elements that need to appear above scrollable content
- Use Level 1 for basic cards and alerts that need subtle separation

### ❌ Don't:

- Don't change the shadow colours
- Don't change the shadow depth
- Only use one shadow at one time
- Don't modify the default elevation of components
- Don't create custom elevation levels outside the defined system
- Don't use multiple elevation levels on a single element
- Don't use elevation levels inconsistently across similar components

## 4. Responsive Behaviour

Elevation levels remain consistent across all breakpoints. The visual appearance of shadows may need slight adjustments for different screen sizes to maintain visual clarity, but the elevation hierarchy should remain the same.

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Small     | Elevation levels maintain same hierarchy | Level 1 cards, Level 2 sticky nav |
| Medium    | Elevation levels maintain same hierarchy | Level 1 cards, Level 2 sticky nav |
| Large     | Elevation levels maintain same hierarchy | Level 1 cards, Level 2 sticky nav |

## 5. Accessibility (A11y)

- **Visual hierarchy:** Elevation helps users understand the structure and layering of the interface, supporting cognitive accessibility
- **Contrast:** Ensure sufficient contrast between elevated elements and their backgrounds to meet WCAG 2.1/2.2 AA standards
- **Motion sensitivity:** For users with motion sensitivity, consider reducing or removing elevation animations where possible
- **Focus indicators:** Elevated interactive elements must have clear focus indicators that are not solely dependent on elevation
- **Screen readers:** Elevation is a visual treatment; ensure semantic HTML and ARIA attributes convey the hierarchy and relationships between elements
- **Keyboard navigation:** Elevated elements (especially modals and overlays) must be keyboard accessible and trap focus appropriately

## 6. Versioning & Change Log

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 2.1     | 2025-01-15 | Removed design-system value tables; to be re-added later. | ✅ Current version |
| 2.0     | 2025-06-20 | Elevation 2.0 guidelines extracted from Figma. Replaces legacy "Shadows" system. | ⚠️ Deprecated |
| 1.0     | Legacy     | Initial shadows system (deprecated) | ⚠️ Deprecated |

**Note:** Legacy/deprecated version: Shadows. The current elevation system (v2.0) replaces the previous shadows-based approach with a more comprehensive elevation system that includes shadows, surface fill colour, and potentially border colour.

---

**Status:** 🟢 Complete and in-sync with code  
**Last updated:** 20th June, 2025

