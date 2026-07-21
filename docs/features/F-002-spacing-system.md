# F-002 — Spacing System (8 Grid)

## Summary

Establish and apply a shared spacing scale throughout HTML Handbook, including the homepage, navigation, cards, dialogs, content modules, and responsive layouts.

## Why

A shared spacing language improves visual consistency, lowers maintenance cost, and makes future responsive decisions easier to explain.

## Problem

The existing stylesheet contains many spacing values, including `6px`, `10px`, `14px`, `18px`, `20px`, `22px`, `28px`, and `36px`. Most do not follow a shared system, making visual rhythm and future maintenance inconsistent.

## Goal

- Use `32`, `24`, `16`, `12`, `8`, and `4` as the default spacing scale.
- Centralize the scale through reusable CSS variables.
- Keep exceptions only when they have a clear optical, structural, or accessibility purpose.
- Preserve the current HTML structure, visual character, responsive behavior, and functionality.

## Scope

- Review and normalize spacing declarations across the primary stylesheet in `index.html`.
- Update desktop and mobile layout spacing where a scale value is appropriate.
- Document unit guidance and the spacing decision.
- Do not alter HTML structure or normalize borders, transforms, element dimensions, or typography as if they were spacing.

## Required Changes

Change the desktop `main` padding:

```css
/* Before */
padding: 28px 36px;

/* After */
padding: 24px;
```

Normalize the mobile `main` padding to `16px`, using the shared scale while preserving the compact responsive layout.

Apply shared tokens to major layout and component spacing:

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-6: 24px;
--space-8: 32px;
```

## Responsive Review

### Keep as `px`

- Component padding and gaps, expressed through the shared `px` spacing tokens.
- Header, sidebar, modal, card, form, homepage, memo, tutorial, issue, and mobile interaction spacing.
- Two compact icon/number controls retain `3px 5px` as documented optical exceptions.

### Change to `rem`

- None in this feature. Typography sizing is outside the approved scope, and converting component spacing would change the current visual rhythm without a demonstrated benefit.

### Change to `%`

- None in this feature. Existing percentage widths already handle fluid containers where needed; the reviewed spacing declarations are component-oriented.

### Change to `clamp()`

- None in this feature. The project does not currently have a hero section or another large fluid spacing region that would justify it.

## Acceptance Criteria

- [x] Desktop `main` padding is `24px` on all sides.
- [x] Mobile `main` padding is normalized to `16px`.
- [x] Project spacing declarations have been reviewed by unit and purpose.
- [x] Shared spacing tokens are created and used by primary layout and UI components.
- [x] Non-scale spacing is limited to documented optical or functional exceptions.
- [x] No HTML structure, color, typography, shadow, or behavior is changed.
- [x] Design System, Roadmap, Decisions, Contribution Workflow, and Feature documentation are updated.
- [x] No duplicate CSS rule is introduced.

## Deliverables

- Updated `index.html` spacing tokens and primary UI spacing.
- Updated Documentation Foundation under `docs/`.
- Recorded D-002 spacing-system decision.
- Reusable Feature documentation template.
