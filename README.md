# Premium Animations

Premium Animations is a Magic Patterns / Agent Skills-compatible skill for generating and refining high-end frontend interfaces with purposeful motion.

It teaches an AI agent how to choose between GSAP, Motion, Lenis, ScrollTrigger, SplitType, SVG animation, Three.js, and React Three Fiber while preserving accessibility, performance, typography, hierarchy, and responsive polish.

## Installation

For the Magic Patterns **Install Skill** dialog, paste exactly this command:

```bash
npx skills add https://github.com/filipe-dev-macae/premium-animations --skill premium-animations
```

Make sure the command includes the skill name after `--skill`.

Install from GitHub with the Skills CLI:

```bash
npx skills add https://github.com/filipe-dev-macae/premium-animations --skill premium-animations
```

For Codex project-level installation, the CLI installs to `.agents/skills/` by default when run inside a project:

```bash
npx skills add https://github.com/filipe-dev-macae/premium-animations --skill premium-animations --agent codex
```

To list available skills before installing:

```bash
npx skills add https://github.com/filipe-dev-macae/premium-animations --list
```

## Usage

After installation, ask your coding agent for UI work that involves premium frontend craft, motion, design polish, or animation architecture.

Example prompts:

```text
Use the premium-animations skill to build a polished SaaS landing page with a scroll-led product walkthrough, GSAP ScrollTrigger for the hero, and Motion for component states.
```

```text
Use premium-animations to audit this dashboard for motion, hierarchy, accessibility, reduced-motion support, and performance.
```

```text
Create a Magic Patterns prompt for an agency portfolio homepage with masked case-study reveals, Lenis smooth scrolling, and restrained premium motion.
```

## How Magic Patterns Loads Skills

Magic Patterns Agent 2.0 supports Skills as specialized instruction files loaded on demand. Compatible skills follow the open Agent Skills format:

- A skill is a directory or repository containing a `SKILL.md`.
- `SKILL.md` starts with YAML front matter.
- The required front matter fields are `name` and `description`.
- The Markdown body contains the instructions the agent loads when the skill is relevant.
- Optional supporting files can live in folders such as `references/`, `examples/`, `scripts/`, or `assets/`.

This repository keeps `SKILL.md` at the repository root so `npx skills add` can discover it without extra flags.
It also includes a mirrored `skills/premium-animations/` package for web importers that expect catalog-style skill repositories.

## Directory Structure

```text
premium-animations/
├── SKILL.md
├── README.md
├── LICENSE
├── examples/
│   ├── agency.md
│   ├── bento-grid.md
│   ├── cards.md
│   ├── cta.md
│   ├── dashboard.md
│   ├── ecommerce.md
│   ├── faq.md
│   ├── feature-grid.md
│   ├── footer.md
│   ├── forms.md
│   ├── hero.md
│   ├── landing-page.md
│   ├── navbar.md
│   ├── portfolio.md
│   ├── pricing.md
│   ├── saas.md
│   ├── testimonials.md
│   └── timeline.md
└── references/
    ├── animation-principles.md
    ├── gsap-philosophy.md
    ├── lenis-philosophy.md
    ├── micro-interactions.md
    ├── motion-philosophy.md
    ├── premium-ui-principles.md
    └── scroll-design.md
└── skills/
    └── premium-animations/
        ├── SKILL.md
        ├── examples/
        └── references/
```

## Best Practices

- Use Motion for component state, layout animation, shared layout, gestures, and AnimatePresence.
- Use GSAP for complex sequences, hero timelines, ScrollTrigger, SplitType, and SVG path animation.
- Use Lenis only when smooth scrolling supports the page type, and synchronize it with ScrollTrigger.
- Use Three.js or React Three Fiber only when 3D is conceptually useful.
- Always support `prefers-reduced-motion`.
- Avoid `transition: all`, decorative over-animation, generic gradient blobs, and inaccessible scroll hijacking.

## Validation

The repository is designed to be discoverable by:

```bash
npx skills add https://github.com/filipe-dev-macae/premium-animations --skill premium-animations --list
```

The expected result is one available skill named `premium-animations`.
