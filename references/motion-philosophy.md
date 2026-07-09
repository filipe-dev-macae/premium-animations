# Motion Philosophy

Use Motion when animation is tied to React state, component lifecycle, layout transitions, gestures, hover, tap, drag, or route-level presence.

## Rules

- Use variants for coordinated groups.
- Use `layout` when object constancy matters.
- Use `layoutId` for shared layout transitions.
- Use `AnimatePresence` for mounting and unmounting.
- Use `whileHover`, `whileTap`, and `whileInView` for small interactions.
- Use `useReducedMotion()` in every meaningful animated component.
- Keep spring motion physical and restrained.
- Avoid Motion and GSAP fighting over the same property.

## Good Uses

- Billing toggles.
- Tabs and active indicators.
- Modals and drawers.
- Cards with real click affordance.
- Form feedback.
- Shared list-to-detail transitions.

## Bad Uses

- Huge scroll narratives that need precise timeline control.
- SVG path drawing that needs stroke control.
- Animating very large data tables.
- Decorative motion with no state or story.
