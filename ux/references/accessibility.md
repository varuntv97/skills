# Accessibility checks

Accessibility means everyone can use the product: people with permanent disabilities
(blindness, low vision, colour blindness, motor or cognitive difficulties),
temporary ones (an injured hand), and situational limits (gloves, glare, noise,
time pressure). Follow general good practice, in the spirit of WCAG's four
principles: perceivable, operable, understandable, robust.

Run the matching section before closing each phase. Record any issue found as a
decision or an assumption.

## Phase 1: Requirements
- Are there legal or contractual accessibility requirements?
- Are any known users likely to have accessibility needs?

## Phase 2: User research
- Did the research consider older, occasional, low-vision or non-native-language
  users, and situational limits (gloves, sunlight, noise)?

## Phase 3: Personas and roles
- Does at least one persona reflect an accessibility need or situational limit, if
  the research supports it?

## Phase 4: Journeys
- Do any stages depend on a single sense (only colour, only sound)?
- Are time-pressured stages designed so slower users can still complete them?

## Phase 5: Information architecture
- Is navigation consistent across screens?
- Are labels plain and predictable?
- Is there more than one way to find important content (navigation and search)?

## Phase 6: Flows
- Can every flow be completed with a keyboard alone?
- Are there time limits? If so, can users extend them?
- Do flows avoid needing precise gestures (drag only, long press only)?

## Phase 7: Interaction design
- Status and errors never rely on colour alone (add text or icons).
- Focus moves sensibly after dialogs open and close, and after errors.
- Errors are announced and linked to their fields.
- Touch targets are at least 44 by 44 pixels on touch devices.
- Motion is minimal and respects reduced-motion settings.
- Users can zoom to 200% without losing content.

## Phase 8: UX writing
- Plain language; short sentences.
- Link and button text makes sense out of context (no "Click here").
- Abbreviations are explained or avoided.

## Phase 9: Wireframes and prototype
- Semantic HTML: real buttons, links, headings, lists, tables and landmarks.
- Every form field has a visible label.
- Visible focus style on every interactive element.
- Text contrast at least 4.5:1 (3:1 for large text and UI boundaries).
- Logical heading order and reading order.
- Images and icons have text alternatives, or are hidden from screen readers if
  decorative.
