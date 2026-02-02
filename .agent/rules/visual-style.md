# Rule: PowerPoint Presentation Generation from Template

## Purpose
This rule defines the EXACT procedure for generating `.pptx` files that are visually identical to the corporate template `course-context/presentation-template.pptx`. The output must look like someone opened the template, replaced placeholder text, and saved — not like a new file was built from scratch.

---

## Critical Principle: CLONE, DON'T CREATE

**NEVER create shapes, text boxes, or formatting from scratch.** The template contains pre-built slide layouts with positioned placeholders, decorative shapes, connector lines, and color-coded rectangles. Your job is to:
1. Load the template as the base presentation
2. Add slides using the template's built-in layouts
3. Write text ONLY into existing placeholders (by index)
4. NEVER add new shapes, text boxes, rectangles, or any other elements
5. NEVER modify placeholder positions, sizes, fonts, or colors
6. NEVER set font name, font size, font color, bold, or alignment on runs/paragraphs — the layout already defines all formatting

---

## Template Specifications

### File
- **Template path**: `course-context/presentation-template.pptx`
- **Slide size**: 13.33 × 7.50 inches (widescreen 16:9)
- **Language**: `en-US`

### Theme: "Custom 95"
| Role | Hex | Name | Usage |
|------|-----|------|-------|
| dk1 (text) | `#000000` | Black | Primary text on light backgrounds |
| lt1 (background) | `#FFFFFF` | White | Title text on dark backgrounds, slide master text |
| dk2 (brand primary) | `#93D24F` | NextGen Lime Green | Main accent color |
| lt2 (light neutral) | `#E7E6E6` | Light Gray | Subtle backgrounds |
| accent1 | `#5AB0F1` | Sky Blue | Secondary accent |
| accent2 | `#EFB233` | Golden Yellow | Warning/alert accent |
| accent3 | `#0CC6D3` | Teal | Tertiary accent |
| accent4 | `#D9A0DF` | Lavender | Quaternary accent |
| accent5 | `#FF3FFF` | Magenta | Reserved |
| accent6 | `#BAE6F4` | Light Cyan | Reserved |
| hlink | `#BAE6F4` | Light Cyan | Hyperlinks |
| folHlink | `#EFB233` | Golden Yellow | Followed hyperlinks |

### Typography (inherited from theme — DO NOT override)
- **Major font (headings/titles)**: Century Gothic
- **Minor font (body text)**: Arial

### Master Slide Background
- Solid fill: scheme color `tx1` with `lumMod=75000` and `lumOff=25000` (dark charcoal gray, approximately `#404040`)
- All layouts inherit this dark background

### Master Slide Text Styles (inherited — DO NOT set manually)
- **Title**: Century Gothic, 30pt, Bold, White (`bg1`), left-aligned, 90% line spacing
- **Body Level 1**: Arial, 28pt, White (`bg1`), left-aligned, 90% line spacing, bullet: `•`
- **Body Level 2**: Arial, 24pt, White, 90% line spacing, bullet: `•`
- **Body Level 3**: Arial, 20pt, White, 90% line spacing, bullet: `•`
- **Body Level 4**: Arial, 18pt, White, 90% line spacing, bullet: `•`
- **Body Level 5**: Arial, 18pt, White, 90% line spacing, bullet: `•`

---

## Available Slide Layouts

### Layout Index 0: "Timeline 1"
**Use for**: Stage-based project timelines with 5 columns and 3 bottom summary boxes.

**Placeholder map** (22 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title (e.g., "PROJECT TIMELINE") |
| 10 | Label column 1 | ADD TEXT | Column 1 label (e.g., "STAGE") |
| 15 | Number column 1 | 00 | Column 1 number (e.g., "01") |
| 20 | Description column 1 | Add text here | Column 1 description |
| 11 | Label column 2 | ADD TEXT | Column 2 label |
| 16 | Number column 2 | 00 | Column 2 number (e.g., "02") |
| 31 | Description column 2 | Add text here | Column 2 description |
| 12 | Label column 3 | ADD TEXT | Column 3 label |
| 17 | Number column 3 | 00 | Column 3 number |
| 32 | Description column 3 | Add text here | Column 3 description |
| 13 | Label column 4 | ADD TEXT | Column 4 label |
| 18 | Number column 4 | 00 | Column 4 number |
| 33 | Description column 4 | Add text here | Column 4 description |
| 14 | Label column 5 | ADD TEXT | Column 5 label |
| 19 | Number column 5 | 00 | Column 5 number |
| 34 | Description column 5 | Add text here | Column 5 description |
| 28 | Bottom box 1 title | ADD TEXT | Bottom left box title |
| 25 | Bottom box 1 body | Add text here | Bottom left box description |
| 29 | Bottom box 2 title | ADD TEXT | Bottom center box title |
| 26 | Bottom box 2 body | Add text here | Bottom center box description |
| 30 | Bottom box 3 title | ADD TEXT | Bottom right box title |
| 27 | Bottom box 3 body | Add text here | Bottom right box description |

**Decorative elements** (non-placeholder, DO NOT touch):
- Large background rectangle behind columns
- 3 bottom rectangles with colored accent bars (accent4=Lavender, accent1=Blue, accent2=Yellow)
- 4 vertical connector lines separating columns

---

### Layout Index 1: "Timeline 2"
**Use for**: Date-based two-row timelines with 4 items per row and numbered circles.

**Placeholder map** (21 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title |
| 10 | Date row 1, item 1 | ADD TEXT | Date label (e.g., "JAN 23") |
| 11 | Date row 1, item 2 | ADD TEXT | Date label |
| 12 | Date row 1, item 3 | ADD TEXT | Date label |
| 13 | Date row 1, item 4 | ADD TEXT | Date label |
| 20 | Desc row 1, item 1 | Add text here | Description |
| 21 | Desc row 1, item 2 | Add text here | Description |
| 22 | Desc row 1, item 3 | Add text here | Description |
| 23 | Desc row 1, item 4 | Add text here | Description |
| 24 | Date row 2, item 1 | ADD TEXT | Date label |
| 25 | Date row 2, item 2 | ADD TEXT | Date label |
| 26 | Date row 2, item 3 | ADD TEXT | Date label |
| 27 | Date row 2, item 4 | ADD TEXT | Date label |
| 28 | Desc row 2, item 1 | Add text here | Description |
| 29 | Desc row 2, item 2 | Add text here | Description |
| 30 | Desc row 2, item 3 | Add text here | Description |
| 31 | Desc row 2, item 4 | Add text here | Description |
| 15 | Circle number 1 | 0 | Number in circle (e.g., "1") |
| 16 | Circle number 2 | 0 | Number in circle (e.g., "2") |
| 17 | Circle number 3 | 0 | Number in circle (e.g., "3") |
| 18 | Circle number 4 | 0 | Number in circle (e.g., "4") |

**Decorative elements** (non-placeholder, DO NOT touch):
- 4 colored rectangles at bottom (dk2=Green, accent3=Teal, accent4=Lavender, accent2=Yellow)
- Circles are styled (ellipse shape, fill=tx1)
- 16 connector lines forming the timeline grid

---

### Layout Index 2: "Timeline 3"
**Use for**: Stage timelines with 5 columns, picture placeholders at the bottom.

**Placeholder map** (21 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title |
| 10-14 | Labels (cols 1-5) | ADD TEXT | Column labels |
| 15-19 | Numbers (cols 1-5) | 00 | Column numbers |
| 30-34 | Descriptions (cols 1-5) | Add text here | Column descriptions |
| 25-29 | Pictures (cols 1-5) | (image placeholder) | Optional pictures |

**Decorative elements**: Background rectangle, 4 vertical connectors, 1 horizontal connector.

---

### Layout Index 3: "Title and SmartArt"
**Use for**: Slides that need a SmartArt diagram with 3 numbered items.

**Placeholder map** (5 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title |
| 10 | SmartArt | (diagram) | SmartArt diagram — see special handling below |
| 15 | Circle number 1 | 0 | Number (e.g., "1") |
| 16 | Circle number 2 | 0 | Number (e.g., "2") |
| 17 | Circle number 3 | 0 | Number (e.g., "3") |

**SmartArt note**: The SmartArt placeholder (idx=10) contains a diagram. python-pptx has LIMITED SmartArt support — you cannot easily modify SmartArt data programmatically. For slides that need categorized content with 3 items, prefer using Layout Index 5 ("Title and Content") with bullet points instead, OR copy the SmartArt slide from template and modify the underlying XML directly.

---

### Layout Index 4: "Milestones"
**Use for**: 4-column milestone layouts with dates, descriptions, and colored accent bars.

**Placeholder map** (13 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title |
| 10 | Label col 1 | ADD TEXT | Month label (e.g., "JAN") |
| 15 | Number col 1 | 00 | Day number (e.g., "23") |
| 30 | Desc col 1 | Add text here | Milestone description |
| 11 | Label col 2 | ADD TEXT | Month label |
| 16 | Number col 2 | 00 | Day number |
| 31 | Desc col 2 | Add text here | Milestone description |
| 12 | Label col 3 | ADD TEXT | Month label |
| 17 | Number col 3 | 00 | Day number |
| 32 | Desc col 3 | Add text here | Milestone description |
| 13 | Label col 4 | ADD TEXT | Month label |
| 18 | Number col 4 | 00 | Day number |
| 34 | Desc col 4 | Add text here | Milestone description |

**Decorative elements**: 4 colored accent bars (accent4, dk2/green, accent2, accent3), connector lines.

---

### Layout Index 5: "Title and Content"
**Use for**: General-purpose slides with title + body text, bullet lists, or simple content.

**Placeholder map** (2 accessible placeholders):
| idx | Role | Default text | What to put here |
|-----|------|-------------|------------------|
| 0 | Title | CLICK TO ADD TITLE | Slide title |
| 1 | Content body | (multi-level bullet text) | Body content with bullet points |

**This is the simplest and most versatile layout.** Use it for:
- KPI dashboards (bullet lists)
- Executive summaries
- Any content that doesn't fit the timeline/milestone layouts
- Text-heavy slides

---

## Python Code Template

Every presentation generation script MUST follow this exact pattern:

```python
from pptx import Presentation

# Step 1: ALWAYS load from template — this inherits theme, layouts, master, colors, fonts
prs = Presentation('course-context/presentation-template.pptx')

# Step 2: Remove the 5 example slides that ship with the template
# The template has 5 pre-filled example slides — we must remove them
# so the output contains ONLY our new content
while len(prs.slides) > 0:
    rId = prs.slides._sldIdLst[0].get(
        '{http://schemas.openxmlformats.org/officeDocument/2006/relationships}id'
    )
    prs.part.drop_rel(rId)
    prs.slides._sldIdLst.remove(prs.slides._sldIdLst[0])

# Step 3: Add slides using template layouts and populate placeholders
def add_slide(prs, layout_index):
    """Add a slide using the specified layout index (0-5)."""
    layout = prs.slide_layouts[layout_index]
    return prs.slides.add_slide(layout)

def set_placeholder_text(slide, idx, text):
    """Set text in a placeholder by index. DO NOT set any formatting."""
    ph = slide.placeholders[idx]
    # Clear existing text and set new text
    ph.text_frame.clear()
    ph.text_frame.paragraphs[0].text = text

# Example: Add a "Title and Content" slide (layout 5)
slide = add_slide(prs, 5)
set_placeholder_text(slide, 0, "My Title")
# For body with multiple paragraphs/bullets:
tf = slide.placeholders[1].text_frame
tf.clear()
tf.paragraphs[0].text = "First bullet point"
p = tf.add_paragraph()
p.text = "Second bullet point"
p = tf.add_paragraph()
p.text = "Third bullet point"
# Bullet formatting (•, indentation, font) is inherited from the layout — DO NOT set it manually

# Example: Add a "Timeline 1" slide (layout 0)
slide = add_slide(prs, 0)
set_placeholder_text(slide, 0, "PROJECT TIMELINE")
set_placeholder_text(slide, 10, "PHASE")     # Column 1 label
set_placeholder_text(slide, 15, "01")         # Column 1 number
set_placeholder_text(slide, 20, "Discovery and stakeholder interviews")  # Column 1 description
set_placeholder_text(slide, 11, "PHASE")     # Column 2 label
set_placeholder_text(slide, 16, "02")         # Column 2 number
set_placeholder_text(slide, 31, "Problem framing and scope definition")  # Column 2 description
# ... continue for all columns and bottom boxes

# Step 4: Save
prs.save('artifacts/output.pptx')
```

---

## ABSOLUTE PROHIBITIONS (Things That Break Template Fidelity)

1. **NEVER use `Presentation()` without the template path** — this creates a blank default PowerPoint with wrong theme
2. **NEVER do `from pptx.util import Inches, Pt` and position shapes manually** — all positioning comes from layouts
3. **NEVER do `run.font.name = ...`** or `run.font.size = ...` or `run.font.color.rgb = ...` — fonts are inherited from the master/layout
4. **NEVER do `run.font.bold = True`** — bold is defined in the master title style
5. **NEVER do `paragraph.alignment = ...`** — alignment is inherited
6. **NEVER do `slide.background.fill.solid()` or set background colors** — backgrounds are inherited
7. **NEVER use `slide.shapes.add_textbox()`** — use only layout placeholders
8. **NEVER use `slide.shapes.add_shape()`** — decorative shapes are in the layout
9. **NEVER use `slide.shapes.add_table()`** — use bullet lists in "Title and Content" layout instead
10. **NEVER use `slide.shapes.add_picture()`** unless filling a PICTURE placeholder (idx 25-29 in layout 2)
11. **NEVER import or use `RGBColor`, `Pt`, `Inches`, `Emu`, `PP_ALIGN`** — these are signs you're overriding template formatting

---

## Handling Multi-Paragraph Content in Placeholders

When a placeholder needs multiple paragraphs (e.g., body content on "Title and Content" layout):

```python
tf = slide.placeholders[1].text_frame
tf.clear()
# First paragraph (replaces the cleared default)
tf.paragraphs[0].text = "First point"
# Additional paragraphs inherit bullet formatting from the layout
for line in ["Second point", "Third point", "Fourth point"]:
    p = tf.add_paragraph()
    p.text = line
```

For Level 2 bullets (sub-items):
```python
p = tf.add_paragraph()
p.text = "Sub-item text"
p.level = 1  # This is the ONLY formatting you may set — indent level (0-4)
```

---

## Slide Removal Method (Deleting Template Example Slides)

The template ships with 5 example slides. You MUST remove them before adding your content. Use this exact code:

```python
# Remove all template example slides
xml_slides = prs.slides._sldIdLst
while len(xml_slides) > 0:
    rId = xml_slides[0].get(
        '{http://schemas.openxmlformats.org/officeDocument/2006/relationships}id'
    )
    prs.part.drop_rel(rId)
    xml_slides.remove(xml_slides[0])
```

---

## Quick Reference: Layout Selection Guide

| Content Type | Layout Index | Layout Name |
|-------------|-------------|-------------|
| General text / bullet lists / KPIs | 5 | Title and Content |
| 5-stage project timeline with bottom summary | 0 | Timeline 1 |
| 8-date two-row timeline with numbered circles | 1 | Timeline 2 |
| 5-stage timeline with icon pictures | 2 | Timeline 3 |
| 3-item categorized content (SmartArt) | 3 | Title and SmartArt |
| 4-column milestones with dates | 4 | Milestones |
