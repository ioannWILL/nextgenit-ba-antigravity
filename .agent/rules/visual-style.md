<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# NextGenIT Presentation Style Guide

This rule defines the strict visual branding and technical execution for all PowerPoint presentations in this project. All `.pptx` files must be generated using `course-context/presentation-template.pptx` as the foundation, with zero manual formatting.

## 1. Visual DNA (Extracted from Template XML)

### A. Theme Color Scheme
The following hex values are the ONLY authorized colors for branding. They must be referenced via their theme roles (`dk1`, `accent1`, etc.), not by hex.

- **Background/Text 1 (dk1)**: `#000000` (Black)
- **Background/Text 1 (lt1)**: `#FFFFFF` (White)
- **Background/Text 2 (dk2)**: `#93D24F` (NextGen Green)
- **Background/Text 2 (lt2)**: `#E7E6E6` (Soft Gray)
- **Accent 1**: `#5AB0F1` (Corporate Blue)
- **Accent 2**: `#EFB233` (Warning Orange)
- **Accent 3**: `#0CC6D3` (Process Cyan)
- **Accent 4**: `#D9A0DF` (Logic Purple)
- **Accent 5**: `#FF3FFF` (Action Magenta)
- **Accent 6**: `#BAE6F4` (Info Blue)
- **Hyperlink**: `#BAE6F4`
- **Followed Hyperlink**: `#EFB233`

### B. Typography
Fonts are managed by the theme. Never specify them in code.
- **Major Font (Headings)**: `Century Gothic`
- **Minor Font (Body)**: `Arial`

## 2. Slide Layout Inventory
Reference layouts by their index in the `slideMaster` for predictable results.

| Index | Layout Name | Common Placeholder Indices |
| :--- | :--- | :--- |
| **0** | **Timeline 1** | Title (0), Stage Labels (10-14), Stage Names (15-19), Descriptions (20-24), Metrics (25-30+) |
| **1** | **Timeline 2** | Alternate Timeline view |
| **2** | **Timeline 3** | Complex Process view |
| **3** | **Title and SmartArt** | Title (0) |
| **4** | **Milestones** | Title (0), Milestone Blocks (10-19), Status Flags (30-34) |
| **5** | **Title and Content** | Title (0), Content Body (1) |

## 3. Technical Execution Rules

### Absolute Prohibitions (The "Never" List)
- **NO Manual Fonts**: Never use `run.font.name`, `run.font.size`, or `run.font.color`.
- **NO Manual Colors**: Never use `RGBColor(r, g, b)`.
- **NO Manual Shapes**: Never use `slide.shapes.add_textbox`, `add_shape`, or `add_picture` (unless explicitly requested for non-templated assets).
- **NO Hardcoded Units**: Never use `Inches()`, `Pt()`, or `Cm()`.
- **NO Manual Formatting**: Never set `bold`, `italic`, or `alignment` on runs.

### Implementation Pattern (The "Only" Way)
1. **Load**: `prs = Presentation('course-context/presentation-template.pptx')`
2. **Clean**: Remove example slides (`slide_id` loop) before adding content.
3. **Add**: `slide = prs.slides.add_slide(prs.slide_layouts[INDEX])`
4. **Populate**: `slide.placeholders[IDX].text = "Your Content"`
5. **Save**: Everything else (fonts, colors, sizes, positions) is inherited automatically.

## 4. Automation Template (Python)

```python
from pptx import Presentation

# 1. Load the NextGenIT Branded Template
template_path = 'course-context/presentation-template.pptx'
prs = Presentation(template_path)

# 2. Add a standard 'Title and Content' slide (Layout Index 5)
# Title placeholder is usually at Index 0
# Content placeholder is usually at Index 1
slide = prs.slides.add_slide(prs.slide_layouts[5])
slide.placeholders[0].text = "Phase 2 Success Metrics"
slide.placeholders[1].text = "• Security Compliance: 100%
• Cost Savings: $48k/year
• Adoption: 80% within 30 days"

# 3. Save as the final deliverable artifact
prs.save('artifacts/project_kpis.pptx')
```
