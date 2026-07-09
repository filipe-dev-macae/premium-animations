# Lenis Philosophy

Lenis is for smooth, premium scrolling on brand, editorial, portfolio, and marketing experiences. It is not a default for dashboards, admin tools, forms, or dense product UIs.

## Rules

- Use one Lenis instance.
- Drive it with a single `requestAnimationFrame` loop.
- Destroy it on cleanup.
- Disable or reduce it for `prefers-reduced-motion`.
- Do not combine with CSS `scroll-behavior: smooth`.
- Test wheel, touchpad, keyboard, anchors, and mobile.

## ScrollTrigger Synchronization

When using GSAP ScrollTrigger:

```ts
lenis.on("scroll", ScrollTrigger.update)

function raf(time: number) {
  lenis.raf(time)
  requestAnimationFrame(raf)
}

requestAnimationFrame(raf)
```

Refresh ScrollTrigger after layout changes and avoid multiple scroll loops.
