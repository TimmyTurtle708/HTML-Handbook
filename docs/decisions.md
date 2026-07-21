# Design Decisions

## D-001 — Default Border Radius

**Decision:** Use `6px` as the default border radius for general UI components.

## D-002 — Spacing System

**Decision:** Adopt an 8 Grid spacing system, using `32`, `24`, `16`, `12`, `8`, and `4` as the standard working scale and exposing these values as shared CSS tokens.

**Reason:** Improve consistency and maintainability while preserving only intentional optical adjustments, accessibility dimensions, and existing responsive behavior.
