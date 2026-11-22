# CyberDEX — V2 Design Guidelines

## Scope
V2 is the UI/UX refinement branch. Preserve the established CyberDEX identity; do not merge V3 development controls into V2 or change production (main) without approval.

## Visual system
- Brand yellow: `#fcee09`; dark background: `#181a1e`; border: `#3a3d40` / `#424b54`.
- Text: `#f4f4f4`; secondary copy: `#c2c4c5`; muted: `#aeb4b6`.
- Use Noto Sans TC for UI and Barlow Condensed for display headings; keep the existing 12/14/16px caption/body/section scale and responsive display typography.
- Preserve existing sharp corners, angular action buttons, dark surfaces, grain, card art, and single yellow border for selected variants. Avoid decorative additional borders or unnecessary containers.
- Keep existing desktop whitespace, price transitions, and pack opening effects.

## Interaction
- Default to Beta before Retail; do not conflate their card prices or images.
- Search supports card number, name, and rarity; matching cards identify edition and rarity. Errors and result counts are announced.
- Keyboard submission moves focus to the result title or first matching card. Pointer users keep their normal workflow.
- Controls use visible, contrasting focus indicators only for keyboard focus; preserve native semantics and Escape behavior. Closed menus must be excluded from tab navigation.
- Expandable ranking rows expose their expanded state. Disabled 30-day ranking choices have an adjacent explanation.
- Respect reduced-motion preferences. Keep chart prices tied to actual dates and never interpolate missing prices.

## Responsive behavior
- Existing breakpoints: 760px (mobile) and 560px (compact ranking).
- Use fluid chart widths on mobile and preserve the selected real price date during resize when a selection is active.
- Aim for 44px minimum touch targets for primary controls, filters and menu options; avoid horizontal scrolling.
- Validate 320, 390, 768 and 1440px widths and keyboard navigation before release.

## Performance and data
- Avoid fetching starter data on ranking/pack-only routes and history data on pack-only routes.
- Keep artwork aspect ratios and graceful missing-image states.
- Label reference-price snapshot dates, sources and currency; never describe them as actual transaction prices.

## Regression checklist
- Home: edition and series, search by number/name/rarity, missing results, single/multiple matches.
- Chart: date filters, pointer and keyboard navigation, resize/orientation, absent history.
- Ranking: both editions, disabled sort reason, expanded rows, more results.
- Pack: picker, gestures, reveal, reset, reduced motion; no V3 dev controls visible.
- Verify deployment of V2 separately. Do not change Main or V3.
