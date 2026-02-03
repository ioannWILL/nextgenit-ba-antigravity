<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 2.3: Stakeholder Alignment & Visual Branding

## Context
A sharp problem statement is only useful if stakeholders buy into it. As a Senior BA, you don't just "send a file"—you tell a story. To maintain professional credibility, your visual materials (slides, diagrams, reports) must follow the **NextGenIT** corporate style.

## Your Task
1. **Define Visual Rules**: Extract the visual "DNA" from the corporate template and document it as a project rule.
2. **Branded Presentation**: Create a Powerpoint presentation that visualizes the metrics from Phase 2, ensuring it is a **clone** of the corporate style in terms of fonts, colors, and layouts.

## IDE Workflow

### Step 1: Establish the Style Guide
Ask me: **"I want to define a specific visual style for all powerpoint slides in this project. Read `course-context/presentation-template.pptx` — extract it as a ZIP, parse every XML file inside (theme, slide master, slide layouts, example slides), and document the EXACT colors, fonts, layout names, placeholder indices, and positioning rules into `.agent/rules/visual-style.md`."**

Explain to the student: the key insight is that a `.pptx` file is actually a ZIP archive containing XML files. The LLM must parse the raw XML to extract precise values — not guess from visual appearance. Recommend using a thinking model for this deep analysis.

### Step 2: Verify the Style Rule
The file `.agent/rules/visual-style.md` must now exist and contain:
- **Theme Color Scheme**: Every color role (dk1, lt1, dk2, lt2, accent1–6, hlink, folHlink) with exact hex values.
- **Typography**: The exact `majorFont` and `minorFont` typeface names from the theme XML `<a:fontScheme>`.
- **Slide Layouts**: A complete map of every layout (by index and name) with every placeholder's `idx`, type, role, and default text.
- **Python Code Template**: A ready-to-use code pattern that loads the template, removes example slides, adds new slides by layout index, and writes text ONLY into placeholders — with ZERO manual formatting.
- **Absolute Prohibitions**: A clear list of what the LLM must NEVER do (add shapes, set fonts, set colors, use Inches/Pt/RGBColor, etc.).

**Key quality check**: If the rule contains lines like `run.font.name = "Century Gothic"` or `slide.shapes.add_textbox(...)` or `from pptx.util import Pt`, it is WRONG. The whole point is that formatting is inherited from the template — never set manually.

### Step 3: Generate the Branded Presentation
Use Antigravity to:
1.  **Branded Slide Generation**: "Following the rule in `.agent/rules/visual-style.md`, generate `artifacts/project_kpis.pptx`. Load `course-context/presentation-template.pptx` as the base, remove the 5 example slides, then add new slides using the template's built-in layouts. Write text ONLY into existing placeholders by index. Do NOT set any fonts, colors, sizes, bold, alignment, or add any shapes — all formatting must be inherited from the template."
2.  **Content source**: "Populate the slides with data from `artifacts/success_metrics.md`. Use Layout 5 (Title and Content) for KPI overview slides with bullet lists. Use Layout 4 (Milestones) for verification milestones. Use Layout 0 (Timeline 1) for rollout phases."

## Deliverables
1. Rule file: `.agent/rules/visual-style.md`.
2. Branded presentation: `artifacts/project_kpis.pptx` (Must be a styled `.pptx` file).

---

**STOP:** Once you have created the branded presentation, open the file to verify if the style, fonts, and colors match the template. I will verify this before we wrap up Phase 2.

**Phase 2 Complete.**
You have transformed chaos into a defined problem, a contained scope, and a professional executive pitch that looks like a real NextGenIT deliverable.
Next: Phase 3 — Reverse Engineering.
