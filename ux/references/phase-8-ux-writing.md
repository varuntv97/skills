# Phase 8: UX writing

**Goal:** Make every word in the product clear, consistent and useful.

**Done when:** Voice and tone are agreed, the patterns below are defined, and every
screen's key text is in the copy deck.

## Voice and tone

- How should the product sound: formal, friendly, neutral? Does it differ between
  internal and customer-facing screens?
- Address users as "you"? Use "we" for the company?
- Words or phrases to avoid (internal jargon, legal-sounding language, blame).

## Patterns to define

**Buttons and links**
- Use verbs that say what happens ("Download invoice", not "Submit" or "OK").
- An action keeps the same name throughout ("Cancel order" button produces an
  "Order cancelled" message).

**Error messages**
- Pattern: what happened, plus how to fix it. No blame, no codes shown alone,
  no vague "Something went wrong" without a next step.
- Example: "We couldn't load your invoices because the connection dropped. Check
  your connection and try again."

**Empty states**
- Explain what will appear here and what the user can do now.

**Confirmations and success messages**
- Say what was done and anything the user should know next.

**Status labels**
- Use the glossary status names from phase 5, phrased for the reader's role.

**Notifications and emails**
- Subject lines and short bodies for each notification from phase 4.

**Help text and field labels**
- Labels are short nouns; hints explain format or purpose; never use placeholder
  text as the only label.

**Formats**
- Dates, times, time zones, numbers, currency, units, and how they appear on mobile.

**Localisation**
- Languages to support. Leave room for longer translations. Avoid text inside
  images.

## Copy deck

For each screen ID, list the key strings: page title, primary and secondary buttons,
empty state, main error messages, success messages, and any helper text. The
prototype in phase 9 must use exactly these strings.

## Traps to probe

- Same concept with different names on different screens: check against the
  glossary.
- System or database terms leaking into the interface.
- Messages that only make sense to the team.

## Spec section 8 structure

8.1 Voice and tone · 8.2 Writing patterns with examples · 8.3 Formats ·
8.4 Localisation · 8.5 Copy deck (table per screen ID) · 8.6 Notification and email
text
