# Design systems

Wireframes are grey-box unless the project provides a design system. When it does,
apply its values to the prototype through the `--ds-*` CSS variables in
`templates/prototype.html`. Never invent brand values that weren't provided.

## What to extract

Whatever the source, aim to capture:
- **Colours:** primary, secondary, background, surface, text, muted text, border,
  success, warning, error, info.
- **Typography:** font families, sizes for headings and body, weights, line heights.
- **Spacing:** the spacing scale (for example 4, 8, 12, 16, 24, 32).
- **Shape:** border radius values, border widths, shadows.
- **Components:** names and variants of buttons, inputs, tables, cards, tags,
  dialogs, navigation. Use these names in the spec so developers can map them.

Record the mapping (design system value → `--ds-*` variable) in spec section 9.3.

## Source: Figma link

1. If Figma tools are available in this session, use them to read variables,
   styles and component names (for example, variable definitions, metadata and
   screenshots of the colour, typography and component pages).
2. Figma's connector may require edit access to the file. If access fails, tell
   the person and offer two options: grant edit access (or duplicate the file into
   their drafts), or export the values (a tokens JSON, CSS, or screenshots of the
   style pages).
3. If no Figma tools are available, ask for an export as above.

## Source: CSS or token files in the repo

1. Look for CSS custom properties, Tailwind config, SCSS variables, or design token
   JSON (for example, files named tokens, theme, variables, colors).
2. Read them and map each value to the matching `--ds-*` variable.
3. Confirm the mapping with the person if names are ambiguous.

## Source: written document or style guide

1. Extract every value the document states.
2. List anything missing (for example, no error colour defined) and ask for it.
   If they don't know, keep the grey-box value for that variable and record an
   assumption.

## Fonts

The prototype must work offline with no external requests. If the design system
uses a web font, list it as the first choice in `--ds-font` followed by system font
fallbacks. Note in section 9.3 that the real font only shows if installed locally.

## Partial design systems

Apply what exists, keep grey-box defaults for the rest, and list the gaps in
section 9.3.
