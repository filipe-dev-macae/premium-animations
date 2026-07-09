# GSAP Philosophy

Use GSAP when animation needs precise orchestration, scroll control, SVG path drawing, SplitType text choreography, nested timelines, or a hero sequence that would become awkward with purely declarative state.

## Rules

- Build the static composition first.
- Create one timeline per narrative moment.
- Use nested timelines for reusable phrases.
- Use labels for sequence readability.
- Use `gsap.context()` in React and clean it up.
- Register plugins deliberately.
- Prefer transforms and opacity.
- Use ScrollTrigger only when scroll position is part of the experience.
- Use SplitType only for short, meaningful text reveals.
- Avoid animating layout properties.

## ScrollTrigger

Synchronize ScrollTrigger with Lenis when smooth scrolling is active. Use `invalidateOnRefresh` for responsive scenes and refresh after fonts, images, or dynamic content change measurements.

## SVG

Use path drawing for diagrams, progress, and technical storytelling. Keep decorative SVGs aria-hidden and informative SVGs accessible.
