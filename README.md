---
description: Functional CSS for the future
---

# Introducing Pollen

Pollen is a library of [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) for rapid prototyping, consistent styling, and as a zero-runtime [utility-first](https://frontstuff.io/in-defense-of-utility-first-css) foundation for your own design systems. Heavily inspired by [TailwindCSS](https://tailwindcss.com).

## What it looks like

Pollen has no runtime, buildstep, class naming conventions, or framework dependencies. It works in stylesheets, inline styles, and CSS-in-JS.

```css
.button {
  font-family: var(--font-sans);
  font-size: var(--scale-00);
  font-weight: var(--font-medium);
  padding: var(--size-2) var(--size-3);
  background: var(--color-blue);
  color: white;
  border-radius: var(--radius);
  box-shadow: var(--elevation-2);
}
```

<button style="all: unset; font-family: sans-serif; font-size:
0.875rem; font-weight: 500; padding: 8px 12px; background: #4299e1; color: white; border-radius: 4px; box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06); cursor: pointer;">Button</button>

## Modules

- [Typography system](modules/typography.md)
- [Color palette](modules/colors.md)
- [Layout scales](modules/layout.md)
- [UI library](modules/ui.md)

## Who's using Pollen

Pollen is used in production by awesome brands in several large-scale websites and projects. Are you using Pollen? [Open an issue on Github](https://github.com/peppercornstudio/pollen/issues/new) to add your site to the list.

- [Corellium](https://www.corellium.com)
- [Inventia](https://inventia.life)
- [Siesta Campers](https://www.siestacampers.com)
- [Faethm](https://faethm.ai)
- [Madeleine Ostoja](https://madeleineostoja.com)
