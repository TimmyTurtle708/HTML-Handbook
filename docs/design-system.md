# Design System

## Border Radius

- Default: `6px`
- Circle: `50%`
- Pill: `9999px`

## Spacing

### Scale

- `32px`
- `24px`
- `16px`
- `12px`
- `8px`
- `4px`

Use this scale for layout spacing, component padding, gaps, and section rhythm whenever practical. New spacing values should use the shared CSS tokens instead of introducing one-off numbers.

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-6: 24px;
--space-8: 32px;
```

Exceptions are limited to documented optical corrections, borders, transforms, and accessibility dimensions such as minimum touch-target height.

For the F-003 desktop hero, the center fortune column remains fixed at `260px`; the Timmy and weather columns use weighted flexible tracks so additional width favors the weather widgets. Below `900px`, the existing responsive flex layout remains authoritative.

### Unit Guidelines

- Components: use `px` for predictable padding, gaps, and touch targets.
- Typography: prefer `rem` when introducing or revising scalable type.
- Containers: use `%` when the element should follow its parent width.
- Hero: consider `clamp()` when a large responsive region needs fluid spacing.
- Preserve existing behavior; do not convert units without a concrete responsive benefit.
