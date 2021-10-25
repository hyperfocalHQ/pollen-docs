---
description: The Grid System
---

# Grid

Pollen comes with an optional set of helpers for creating and maintaining CSS grids in a project. Add it to your project by importing its CSS file

{% code title="With javascript" %}
```javascript
import 'pollen-css/addons/grid.css';
```
{% endcode %}

{% code title="From Unpkg CDN" %}
```markup
<link rel="stylesheet" href="https://unpkg.com/pollen-css/addons/grid.css" />
```
{% endcode %}

## Page Grid

A configurable grid designed to be used for page containers, with a main center column for content and gutters on each side. The main center column will expand until it reaches a max-width, at which point it will remain constrained and centered at that width.&#x20;

Give all children of the grid a `--grid-page-main` column value (equal to `2/3`) to place them in the main content area. Easily "break out" of the page grid for full-width panels by giving a child a `1 / -1` column placement

| Property           | Applies to              |
| ------------------ | ----------------------- |
| `--grid-page`      | `grid-template-columns` |
| `--grid-page-main` | `grid-column`           |

```css
.page {
  display: grid;
  grid-template-columns: var(--grid-page);
}

.page > * {
  grid-column: var(--grid-page-main);
}

.page > .fullwidth {
  grid-column: 1 / -1;
}
```

### Configuration

Each aspect of the page grid is configurable with CSS variables. Set them either on the `:root` pseudo-element to apply globally, or on an individual page grid to apply just for that element.

| Property             | Default           | Description                                                          |
| -------------------- | ----------------- | -------------------------------------------------------------------- |
| `--grid-page-width`  | `var(--width-xl)` | Max width of the main content area                                   |
| `--grid-page-gutter` | `5vw`             | Width of the page gutters until the content area max with is reached |

```css
:root {
 --grid-page-gutter: var(--size-10);
 --grid-page-width: var(--width-lg);
 }
```

## Grid Template

Helpers for quickly setting common grid templates

| Property Group | Applies to                                       |
| -------------- | ------------------------------------------------ |
| `--grid-`      | `grid-template-columns` and `grid-template-rows` |

```css
.grid {
  display: grid;
  grid-template-columns: var(--grid-12);
}
```

| Property    | Value                        |
| ----------- | ---------------------------- |
| `--grid-2`  | `repeat(2, minmax(0, 1fr))`  |
| `--grid-3`  | `repeat(3, minmax(0, 1fr))`  |
| `--grid-4`  | `repeat(4, minmax(0, 1fr))`  |
| `--grid-5`  | `repeat(5, minmax(0, 1fr))`  |
| `--grid-6`  | `repeat(6, minmax(0, 1fr))`  |
| `--grid-7`  | `repeat(7, minmax(0, 1fr))`  |
| `--grid-8`  | `repeat(8, minmax(0, 1fr))`  |
| `--grid-9`  | `repeat(9, minmax(0, 1fr))`  |
| `--grid-10` | `repeat(10, minmax(0, 1fr))` |
| `--grid-11` | `repeat(11, minmax(0, 1fr))` |
| `--grid-12` | `repeat(12, minmax(0, 1fr))` |
