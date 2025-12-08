# Figma Foundations Guidelines Extraction

## Overview

This project extracts **Foundations guidelines** from a Figma file using Figma MCP tools in Cursor and converts them into a clean markdown document formatted for Figma Make's "Guidelines" panel.

## What We Did

1. **Explored the Figma file** using Figma MCP tools (`get_metadata` and `get_design_context`)
2. **Identified the Grid & Breakpoints section** (node ID: `1447:2257`)
3. **Extracted content** including:
   - Screen sizes and breakpoints
   - Grid configurations (Small, Medium, Large, XLarge)
   - Usage guidelines
   - System values and specifications
4. **Created structured markdown** following the GDS Design Documentation Framework
5. **Added TODO placeholders** for foundations not yet found in the Figma file (Colour, Typography, Spacing, Elevation)

## Original Prompt

```
You are helping me extract **foundations guidelines** from a Figma file using the Figma MCP tools in Cursor and turn them into a clean markdown document for Figma Make.

### Goal

Generate a single markdown file called `foundations-guidelines.md` that documents our **Foundations** in a way that fits Figma Make's "Guidelines" panel:

- Colour
- Typography
- Spacing
- Grid & Breakpoints
- Elevation

The markdown must:

- Be based on **existing text** in the Figma file (foundations pages/frames, notes, and guidelines).
- Use **UK English**.
- Follow our **GDS Design Documentation Framework** structure adapted for foundations.
- Focus heavily on **accessibility and white-labelling**.
- Be safe to paste directly into Figma Make (no extra explanation or chatty text).

### What to read from Figma (via Figma MCP)

Using the available Figma MCP tools in this environment:

1. Inspect the current Figma file and:
   - Find pages and frames named or containing:
     - "Foundations", "Foundation"
     - "Colour", "Color"
     - "Typography", "Type"
     - "Spacing"
     - "Grid", "Breakpoints"
     - "Elevation", "Shadow"
   - Within those frames, extract:
     - Text layers describing what the foundation is, when to use it, constraints, and examples.
     - Any notes about accessibility, WCAG, contrast, minimum sizes, responsive behaviour, etc.
     - Any references to system values, variables, and naming conventions.
     - Any "Do / Don't" lists, rules of thumb, or best practices.
     - Any versioning or change-log notes (even if they're informal).

2. **Do not invent guidelines**. If something isn't present in the Figma content:
   - Leave a clear `TODO:` note in the markdown instead of guessing.
   - Example: `TODO: Add explicit accessibility contrast rules for Elevation system.`

3. Prefer **quoting or lightly editing** the existing Figma text for clarity and consistency.

### Documentation structure (per foundation)

For **each foundation** (Colour, Typography, Spacing, Grid & Breakpoints, Elevation), create a section with this structure:

```md
## <Foundation Name>

### 1. Overview
- **What it is:** (1–2 sentences in plain UK English)
- **When to use:** (bullet list of common scenarios)
- **When not to use:** (bullet list of anti-patterns)
- **Accessibility note:** (short note, e.g. WCAG contrast, minimum size, motion, etc.)

### 2. System Structure
Explain how the system is structured for this foundation and how it supports **white-labelling** across brands.

Describe the system values, specifications, and organisation. Include any relevant tables or lists of values that define the foundation system.

### 3. Usage Guidelines

Summarise the **dos and don'ts** from the Figma file.

- **✅ Do:**
  - Turn key "good usage" points into bullets.

- **❌ Don't:**
  - Turn key "misuse" points into bullets.

When possible, reference system values instead of raw values (e.g. use system typography styles rather than specific font sizes).

### 4. Responsive Behaviour (if applicable)

Include this section for **Typography**, **Grid & Breakpoints**, and cases where spacing changes across viewports.

Describe how this foundation behaves across breakpoints using a table where useful:

| Breakpoint | Behaviour / rule | Example |
|-----------|------------------|---------|
| Small     | …                | …       |
| Medium    | …                | …       |
| Large     | …                | …       |

If the Figma file includes references to specific breakpoint values, include them and how they drive behaviour.

### 5. Accessibility (A11y)

Extract and consolidate all accessibility notes for that foundation:

- Relevant **WCAG 2.1/2.2 AA** rules (e.g. colour contrast, minimum tap target, readable text sizes).
- Any **focus, outline, elevation, motion, or typography** guidance tied to accessibility.
- Any **system values** specifically used for accessibility (e.g. focus outlines, high-contrast palettes).

Use a simple checklist-style format where possible.

### 6. Versioning & Change Log

If the Figma file contains dates or notes about changes, add a small table:

| Version | Date       | Change                              | Impact |
|---------|------------|--------------------------------------|--------|
| 1.0     | 2025-??-?? | Initial guidelines extracted to MD. | ✅ Baseline |

If there's no change history, create an initial version row and mark further items as `TODO`.

---

### Output requirements

- Return **only** the final markdown for `foundations-guidelines.md` – no extra commentary.
- The sections must appear in this order:
  1. Colour
  2. Typography
  3. Spacing
  4. Grid & Breakpoints
  5. Elevation

- Within each section, use exactly the headings specified above.
- Use **UK spelling** throughout (e.g. "colour", "organisation", "optimise").
- Do not invent new system values; reuse whatever appears in the Figma file. If a value isn't clear, add a `TODO` instead of guessing.
- Make sure tables are valid markdown and will render correctly in Figma Make.

Now, using the Figma MCP tools, inspect the current Figma file, extract the foundations guidance following these rules, and produce the final `foundations-guidelines.md` content.
```

## Process Summary

### Step 1: Initial Exploration
- Used `mcp_Figma_Desktop_get_metadata` to explore the Figma file structure
- Identified the "Grids & Breakpoints" section (node ID: `1447:2257`)

### Step 2: Content Extraction
- Used `mcp_Figma_Desktop_get_design_context` to extract detailed content from the Grid & Breakpoints section
- Extracted text layers, breakpoint information, grid configurations, and usage guidelines

### Step 3: Markdown Generation
- Created structured markdown following the specified template
- Filled in Grid & Breakpoints section with extracted content
- Added TODO placeholders for missing foundations (Colour, Typography, Spacing, Elevation)

### Step 4: File Creation
- Created `foundations-guidelines.md` with UK English spelling
- Ensured all tables are valid markdown
- Structured content for direct paste into Figma Make

## Current Status

✅ **Completed:**
- Grid & Breakpoints foundation (fully extracted and documented)
- Colour foundation (fully extracted and documented)
- Typography foundation (fully extracted and documented)
- Spacing foundation (fully extracted and documented - v2.1)
- Elevation foundation (fully extracted and documented - v2.1)

## Improvements for Future Prompts

### 1. **Provide Specific Node IDs or Page Names**
**Current issue:** The prompt asks to "find pages and frames named or containing..." but doesn't provide specific locations.

**Improvement:**
```
If you have specific node IDs or page names for each foundation, provide them upfront:
- Colour: node-id=XXX-XXX or page name "Colour Foundation"
- Typography: node-id=YYY-YYY or page name "Typography Foundation"
- etc.
```

**Why:** This would allow direct navigation to the correct sections instead of exploratory searching.

### 2. **Specify Figma File Structure**
**Current issue:** The prompt assumes all foundations are in one file, but they might be in separate pages or files.

**Improvement:**
```
Before starting, please confirm:
- Are all foundations in a single Figma file?
- Are they on separate pages within the file?
- What are the page names?
- Are there any hidden layers or frames we should check?
```

**Why:** Understanding the file structure upfront would make extraction more efficient.

### 3. **Add System Value Extraction Examples**
**Current issue:** The prompt mentions extracting system values but doesn't specify how to identify them in Figma.

**Improvement:**
```
When extracting system values, look for:
- Figma Variables (if using Variables feature)
- Text layers with system value notation
- Component properties that reference system values
- Style names that follow naming conventions
- Any documentation frames that list system values
```

**Why:** This would help identify where system value information might be stored in Figma.

### 4. **Clarify "Do/Don't" Extraction**
**Current issue:** The prompt asks for "Do / Don't" lists but doesn't specify how to identify them.

**Improvement:**
```
When looking for usage guidelines, check for:
- Frames titled "Do" and "Don't" or "✅" and "❌"
- Side-by-side comparison examples
- Text layers with explicit "Do:" or "Don't:" prefixes
- Annotations or notes attached to components
- Any visual examples showing correct vs incorrect usage
```

**Why:** This would help locate usage guidelines that might be presented visually rather than as text.

### 5. **Add Accessibility Extraction Guidance**
**Current issue:** The prompt mentions extracting accessibility notes but doesn't specify where they might be.

**Improvement:**
```
When extracting accessibility information, look for:
- Text layers mentioning "WCAG", "AA", "AAA", "contrast", "accessibility"
- Notes or annotations on components
- Separate accessibility documentation frames
- System value names containing "a11y", "accessibility", "focus", "outline"
- Any contrast ratio values or minimum size specifications
```

**Why:** Accessibility information might be scattered or in specific documentation sections.

### 6. **Specify Output Format Validation**
**Current issue:** The prompt mentions "safe to paste directly into Figma Make" but doesn't specify what that means.

**Improvement:**
```
Before finalising, validate:
- All markdown tables render correctly (test with a markdown previewer)
- No special characters that might break Figma Make's parser
- Headings follow proper hierarchy (## for main sections, ### for subsections)
- Code blocks use backticks correctly
- No HTML tags (use markdown only)
```

**Why:** This would ensure the output works correctly in the target system.

### 7. **Add Progress Reporting**
**Current issue:** The prompt doesn't ask for progress updates when multiple foundations need extraction.

**Improvement:**
```
When extracting multiple foundations:
1. First, report which foundations you found in the Figma file
2. Extract each foundation one at a time
3. Report completion status for each
4. Note any missing information with specific TODO markers
```

**Why:** This would provide better visibility into what was found vs. what's missing.

### 8. **Clarify System Architecture**
**Current issue:** The prompt doesn't specify how to document the system architecture.

**Improvement:**
```
Before documenting the system, verify:
- How is the system structured in the Figma file?
- Are there multiple layers or categories?
- What naming convention is used in the file?
- Are system values documented in variables, text layers, or separate documentation?
```

**Why:** This would ensure the documentation matches the actual system structure in use.

## Recommended Next Steps

1. **Locate missing foundations:** Search the Figma file for pages/frames containing Colour, Typography, Spacing, and Elevation content.

2. **Extract system information:** Look for Figma Variables or system documentation within the file.

3. **Complete TODO sections:** Once all foundations are located, fill in the TODO placeholders with actual content.

4. **Validate output:** Test the markdown file in Figma Make to ensure proper rendering.

5. **Add versioning:** Update the change log with actual dates and version numbers once content is complete.

## Tools Used

- **Figma MCP Tools:**
  - `mcp_Figma_Desktop_get_metadata` - Explore file structure
  - `mcp_Figma_Desktop_get_design_context` - Extract detailed content
  - `mcp_Figma_Desktop_get_screenshot` - Visual reference (if needed)

- **Cursor Tools:**
  - `write` - Create markdown file
  - `read_file` - Review existing content
  - `codebase_search` - Search for related content

## Notes

- The current extraction focused on the Grid & Breakpoints section because it was the most visible/accessible in the Figma file.
- Other foundations may be in separate pages, hidden layers, or require different navigation paths.
- The TODO placeholders ensure the document structure is complete even when content is missing.
- UK English spelling has been applied throughout (e.g., "colour", "behaviour", "optimise").

---

**Last Updated:** 2025-01-15  
**Status:** All foundations complete. Design-system value tables removed for now; will be added in a later update.


