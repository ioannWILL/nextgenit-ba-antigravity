# Lesson 6.1: Wireframes from Requirements

## Context
A BA often acts as a bridge to Design. You need to show the layout of the "Governed AI" dashboard, specifically the security toggles and the quota indicator.

## Your Task
Create a textual wireframe mock-up (using Markdown tables or ASCII) or an HTML snippet that represents the main user interface.

## IDE Workflow

### Step 1: Why BAs Create Wireframes

**Say:**

"You might think wireframes are a designer's job. But here's the reality: in fast-moving projects, the BA is often the first to visualize requirements. Why?

1. **Requirements become real**: A bullet point saying 'show quota usage' is abstract. A wireframe showing a progress bar with '75% of daily tokens used' is concrete.
2. **Stakeholder alignment**: Priya can look at a wireframe and say 'Yes, that's what I meant' or 'No, the dashboard should show team usage, not just mine.'
3. **Developer clarity**: Engineers can estimate work better when they see a layout, not just a list of features.

We're not doing pixel-perfect design. We're doing *functional wireframes* — showing where features live and how users interact with them."

**STOP:** Ask: "Wireframes bridge the gap between requirements and design. Have you created wireframes before, or worked with designers who do? Let me know when you're ready to sketch the dashboard."

---

### Step 2: Dashboard Layout Planning

**Say:**

"Let's think about what the 'Governed AI' dashboard needs to show. Based on our requirements:

**For Developers:**
- Chat interface (main area)
- Quota indicator (how much usage remaining)
- History sidebar (past conversations)

**For Admins/Security:**
- Settings panel (PII filter toggles, RBAC config)
- Audit log viewer
- Team usage dashboard

The challenge: How do we show different views based on role (RBAC)? A Developer shouldn't see Admin settings."

Use Antigravity to:
1. **Layout Design**: "Design an HTML wireframe for the 'Governed AI Developer Dashboard'. Include:
   - A header with user info and role badge
   - A sidebar with: Chat History, Settings (if role permits), Help
   - Main area: Chat interface with prompt input
   - A quota indicator showing 'X tokens used / Y daily limit'
   - Use Tailwind CSS for quick styling
   - Add comments in the HTML explaining what each section does"

**STOP:** After generating the wireframe, ask: "This is the basic developer view. Notice the quota indicator — that addresses Sam's concern about runaway costs. Does the layout feel intuitive? Any key elements missing?"

---

### Step 3: Permission-Based UI Variations

**Say:**

"RBAC isn't just about backend permissions — it affects what users *see*. A Contractor shouldn't even see the 'Admin Settings' menu item. This is called 'permission-based UI' or 'UI trimming.'

Let's create two variants:
1. **Developer view**: Standard dashboard
2. **Admin view**: Same dashboard plus admin controls

The difference shows how RBAC manifests in the UI."

Use Antigravity to:
1. **Role Variants**: "Modify the dashboard wireframe to show two versions:
   - **Developer View**: Chat, history, personal quota, settings (limited)
   - **Admin View**: Everything above PLUS: Team quota dashboard, Audit log access, PII filter configuration, User management link

   Use conditional comments or a toggle to show the difference. Highlight what's hidden from non-admins."

**STOP:** After generating the variants, ask: "Compare the two views. The Admin sees more options, but the core experience is the same. This is how RBAC should feel — seamless for users, but enforced consistently. Does this match the RBAC matrix from Phase 4?"

---

### Step 4: Wireframe Documentation

**Say:**

"Let's document the wireframe decisions. This becomes a reference for designers and developers — explaining *why* things are placed where they are."

Use Antigravity to:
1. **Wireframe Notes**: "Create documentation for the wireframe that explains:
   - Layout rationale (why sidebar vs top nav?)
   - RBAC UI rules (what each role sees/doesn't see)
   - Key interactions (what happens when user clicks 'Submit Prompt'?)
   - Accessibility considerations (keyboard navigation, screen reader hints)"

---

## Deliverables
Ask me to create `artifacts/wireframes.md` with layout documentation and decisions.
Ask me to create `artifacts/preview.html` with the interactive HTML wireframe.

**STOP:** After creating the artifacts, ask: "Wireframes and HTML preview are ready. Open `artifacts/preview.html` in a browser to see the layout:
- Does the dashboard structure support the user stories from Phase 5?
- Is the quota indicator visible enough?
- Would Priya (PM) approve this layout for her team?

Ready for the interactive prototype in Lesson 6.2?"

---
Move to Lesson 6.2.
