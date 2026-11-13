# Phase 7: Interaction design

**Goal:** Define how the product behaves in every situation, including all the
unhappy ones.

**Done when:** Every screen in the inventory has its states defined, and the
product-wide behaviour rules below are all decided.

## Product-wide rules (decide once, apply everywhere)

- **Feedback:** how the product confirms actions (inline message, toast, page
  change). How long messages stay.
- **Loading:** skeletons, spinners or progress for slow actions. What happens if
  loading takes over 10 seconds?
- **Validation:** when fields are checked (on leaving the field, on submit), where
  errors appear, and how the first error is brought into view.
- **Destructive actions:** which actions need confirmation, and which offer undo
  instead. Prefer undo for frequent actions; confirmation for rare, irreversible ones.
- **Drafts and autosave:** is unsaved work kept if the user leaves or loses
  connection?
- **Concurrency:** what happens when two people edit the same record.
- **Session expiry:** warning before timeout? Is work preserved after logging back in?
- **Offline or poor connection:** what still works, and what the user sees.
- **Lists:** pagination, "load more" or infinite scroll; bulk selection and bulk
  actions; empty search results.
- **Tables on small screens:** convert to cards, scroll horizontally, or hide
  columns? Which columns survive on mobile?
- **Notifications:** in-app centre, badges, email, other channels; read and unread
  behaviour.
- **Downloads and exports:** formats, what happens for large exports.
- **Keyboard:** shortcuts for frequent actions; full keyboard operation everywhere.

## Per screen: states

For every screen in the inventory, define each state that can occur:

| State | Question to answer |
|-------|--------------------|
| Default | What does it show with typical data? |
| Loading | What appears while data loads? |
| Empty (first use) | What does a new user see, and what should they do next? |
| Empty (no results) | What appears when a search or filter finds nothing? |
| Partial | What if some data is missing or still syncing? |
| Error | What if loading or saving fails? How do they recover? |
| Success | How is a completed action confirmed? |
| No permission | What does someone without access see? |
| Offline | What if the connection drops? |

Not every state applies to every screen; record "not applicable" explicitly so it's
clear the state was considered.

## Per screen: interactions

- Primary action and secondary actions.
- What each control does, including disabled conditions.
- Behaviour differences between desktop, tablet and mobile.

## Traps to probe

- Only the happy path defined: walk through each state in the table.
- Double submission: is the button disabled while saving?
- Error messages that lose what the user typed.
- Integration failures (from phase 1): what the user sees when the source system is
  down or data is stale. Show "last updated" times where freshness matters.

## Spec section 7 structure

7.1 Product-wide behaviour rules · 7.2 Responsive behaviour rules · 7.3 Per-screen
states and interactions (table per screen, by screen ID) · 7.4 State diagrams for
complex objects (Mermaid `stateDiagram-v2`)
