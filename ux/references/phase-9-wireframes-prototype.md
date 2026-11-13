# Phase 9: Wireframes and prototype

**Goal:** Build a clickable, responsive wireframe prototype of every screen in every
flow, so the team can experience the product before it's built.

**Done when:** Every screen ID in the inventory exists in the prototype, in every
applicable state, for every role that sees it, and every flow can be clicked through
from start to finish.

## Step 1: Confirm before building

Grill on these before writing any HTML:

1. **Screen inventory:** show the full list from phase 6 and confirm nothing is
   missing or extra.
2. **Layout per screen:** for each screen, confirm its purpose, the single most
   important thing on it, its primary action, and the content in priority order.
   Batch similar screens together (for example, all list screens).
3. **Sample data:** propose a realistic data set and confirm it. Use realistic
   names, companies, reference numbers, dates, amounts and statuses that match the
   domain and glossary. Include edge cases: long names, zero values, every status,
   overdue items, very long lists.
4. **Design system:** confirm whether to stay grey-box or apply the design system
   (see `design-system.md`).

## Step 2: Build

Start from `templates/prototype.html`. It already contains the review toolbar,
routing, role, state and device switching, toast messages, and grey-box styles. Read
the comments at the top of the template before editing.

Rules:
- **Every screen, every state, every role.** Use the screen IDs from the inventory
  as the screen keys. States come from the phase 7 tables.
- **Text comes from the copy deck** in phase 8, word for word.
- **Labels come from the glossary.**
- **Links work.** Every button and link that leads somewhere navigates to the right
  screen. Actions that would change data show the success message from the copy
  deck as a toast, and update the sample data where that helps the flow make sense.
- **Responsive.** Use the container query breakpoints already in the template so the
  device switcher shows true desktop, tablet and mobile layouts. Apply the
  responsive rules from phase 7 (for example, tables becoming cards on mobile).
- **Accessible.** Real buttons and links, labelled form fields, visible focus,
  sufficient contrast, logical heading order. See `accessibility.md`.
- **No external libraries, fonts or images.** It must work offline from the file
  system. Use simple inline SVG or grey boxes for icons and images.
- **Grey-box by default.** Greys only, one system font, no brand colours. Hierarchy
  comes from size, weight, spacing and position. If a design system is provided,
  map its values to the `--ds-*` variables in the template rather than restyling
  each element.
- **Annotations.** Fill in each screen's `notes` with its purpose, flows and key
  decision IDs. Reviewers can show them with the annotation toggle.

## When to split into multiple files

Keep one `prototype.html` unless either is true:
- More than about 40 screens, or
- The file would exceed about 400 KB.

If so, split by module (top-level section from phase 5):
- `prototype/index.html`: links to every module and lists all screens by ID.
- `prototype/assets/core.js` and `prototype/assets/core.css`: the shared toolbar,
  router and styles (moved out of the template unchanged).
- `prototype/assets/data.js`: the shared sample data.
- `prototype/<module>.html`: that module's screens, loading the shared assets with
  relative paths, which still works offline.

Tell the person before splitting, and record it as a decision.

## Step 3: Verify

Before showing the result:
- Compare the prototype's screen list with the inventory. Report any gap.
- Click through each flow in order, including error paths.
- Check each screen at all three device sizes.
- Check that every role sees only what the permissions matrix allows.

## Spec section 9 structure

9.1 Screen list with layout notes (purpose, priority order, primary action) ·
9.2 Sample data description · 9.3 Design system applied (or grey-box) ·
9.4 How to use the prototype (controls) · 9.5 Known gaps or simplifications
