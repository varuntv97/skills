# Phase 5: Information architecture

**Goal:** Decide how all content and features are organised, named and found, for
each role.

**Done when:** There is an agreed object model, a sitemap per role, a navigation
model, search and filter rules, and every label is in the glossary.

## Step 1: Object inventory

List every "thing" users deal with (for example: quote, sales order, shipment,
invoice, user, company). For each object, capture:

- What it is, in the users' own words (add to glossary).
- Relationships (one quote becomes one or more orders; one order has many
  shipments).
- Lifecycle statuses, with plain-language labels and who or what changes them.
- The fields users need to see, in priority order, per role. Ask which three fields
  matter most in a list view.
- Which system owns the data (from phase 1 integrations).

Draw the relationships as a Mermaid `erDiagram` or `flowchart`.

## Step 2: Navigation model

- Top-level sections per role. Aim for 5 to 7 at most.
- Home or dashboard content per role: what should someone see first when they log in?
  Tie this back to the most frequent tasks and moments that matter from phase 4.
- Navigation pattern per device (sidebar on desktop, bottom bar or menu on mobile).
- Deep linking: can a link in an email open a specific record directly?
- Global elements: search, notifications, profile, help, company switcher.

## Step 3: Finding things

- Global search: which objects, which fields (numbers, names, references)?
- Filters and sorting per list, with default sort order.
- Saved views or favourites?
- Expected list sizes (from phase 1 volumes) to decide pagination.

## Step 4: Labels

- Use the users' words, not internal or system terms. Confirm each label.
- One label per concept across the whole product (glossary).
- Check status names make sense to the role reading them (a customer may need
  "In production" rather than an internal step name).

## Traps to probe

- Navigation mirroring the company's departments instead of user tasks.
- Internal codes or abbreviations shown to external users.
- Too many top-level sections: ask what could be merged or moved.

## Optional user-question suggestions

If labels or grouping are uncertain, add a user question suggesting a quick card
sort (users group items themselves) or tree test (users find items using only the
menu structure).

## Spec section 5 structure

5.1 Object model and relationships · 5.2 Status definitions per object ·
5.3 Sitemap per role (Mermaid) · 5.4 Navigation per device · 5.5 Home/dashboard
content per role · 5.6 Search, filter and sort rules · 5.7 Labelling decisions
