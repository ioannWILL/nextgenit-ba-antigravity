# Visual Style Rules: NextGenIT Corporate Identity

## Analysis of Source: `course-context/presentation-template.pptx`

Based on the deep analysis of the corporate template theme and layouts, the following visual identity must be applied to all project artifacts:

### 1. Color Palette (NextGenIT 2026 Core)
- **Primary Branding (dk2)**: **#93D24F** (NextGen Lime Green). Used for main accents and highlights.
- **Secondary Branding (accent1)**: **#5AB0F1** (Sky Blue). Used for alternative accents.
- **Warning/Alert (accent2)**: **#EFB233** (Golden Yellow). Used for risks and items requiring attention.
- **Backgrounds (lt2/lt1)**: **#E7E6E6** (Light Gray) or **#FFFFFF** (Pure White).
- **Text (dk1)**: **#000000** (Black) or Deep Gray for primary readability.

### 2. Typography
- **Major Font (Headings)**: **Century Gothic**. Must be used for all slide titles and high-level headers.
- **Minor Font (Body)**: **Arial**. Used for all bullet points, descriptive text, and notes.

### 3. Layout Principles
- **Clarity and Spacing**: Use the "Title and Content" layout (Index 5) for general deliverables.
- **Visual Flow**: The template emphasizes a "Timeline" aesthetic. Use linear visual structures where possible to show progress.
- **Consistency**: All slides MUST inherit formatting from the master slides in `course-context/presentation-template.pptx`. Do not use default PowerPoint styling.

## Implementation Guidelines
- When generating `.pptx` files, always use `Presentation('course-context/presentation-template.pptx')` as the constructor to inherit the theme and master layouts.
- Map project data to the specific color codes above (#93D24F, #5AB0F1, #EFB233) instead of generic "green" or "blue".
