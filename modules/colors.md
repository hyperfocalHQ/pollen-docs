---
description: Rapid visual prototyping
---

# Colors

Pollen includes a default color palette for rapid prototyping as a better alternative to browser defaults. It's designed to be a robust base that you can either replace or adapt from as your project evolves.

## The Palette

| Property group | Applies to                   |
| -------------- | ---------------------------- |
| `--color-*`    | `color` , `background-color` |

Pollen borrows from and lightly adapts Tailwind's excellent [color palette](https://tailwindcss.com/docs/customizing-colors).

Each color has a family of shades ranging from `50` (very light) to `950` (very dark). The unsuffixed color (eg: `--color-red`) in each family is an alias for median in that family (eg: `--color-red-500`).

```css
.alert {
  color: var(--color-red);
}
```

### Greyscale

<table><thead><tr><th width="263">Property</th><th>Value</th></tr></thead><tbody><tr><td><code>--color-grey</code></td><td><code>var(--color-grey-500)</code></td></tr><tr><td><code>--color-grey-50</code></td><td><code>#f9fafb</code></td></tr><tr><td><code>--color-grey-100</code></td><td><code>#f2f4f5</code></td></tr><tr><td><code>--color-grey-200</code></td><td><code>#e8eaed</code></td></tr><tr><td><code>--color-grey-300</code></td><td><code>#d4d7dd</code></td></tr><tr><td><code>--color-grey-400</code></td><td><code>#a5aab4</code></td></tr><tr><td><code>--color-grey-500</code></td><td><code>#767c89</code></td></tr><tr><td><code>--color-grey-600</code></td><td><code>#555d6e</code></td></tr><tr><td><code>--color-grey-700</code></td><td><code>#3f4754</code></td></tr><tr><td><code>--color-grey-800</code></td><td><code>#2c343f</code></td></tr><tr><td><code>--color-grey-900</code></td><td><code>#10181C</code></td></tr><tr><td><code>--color-black</code></td><td><code>#14141B</code></td></tr></tbody></table>

### Red

| Property          | Value                  |
| ----------------- | ---------------------- |
| `--color-red`     | `var(--color-red-500)` |
| `--color-red-300` | `#fc8181`              |
| `--color-red-500` | `#e53e3e`              |
| `--color-red-700` | `#c53030`              |

### Green

| Variable            | Value                    |
| ------------------- | ------------------------ |
| `--color-green`     | `var(--color-green-500)` |
| `--color-green-300` | `#9ae6b4`                |
| `--color-green-500` | `#48bb78`                |
| `--color-green-700` | `#2f855a`                |

### Blue

| Variable           | Value                   |
| ------------------ | ----------------------- |
| `--color-blue`     | `var(--color-blue-500)` |
| `--color-blue-300` | `#63b3ed`               |
| `--color-blue-500` | `#4299e1`               |
| `--color-blue-700` | `#3182ce`               |

### Pink

| Property           | Value                   |
| ------------------ | ----------------------- |
| `--color-pink`     | `var(--color-pink-500)` |
| `--color-pink-300` | `#fbb6ce`               |
| `--color-pink-500` | `#ed64a6`               |
| `--color-pink-700` | `#d53f8c`               |

### Purple

| Property             | Value                     |
| -------------------- | ------------------------- |
| `--color-purple`     | `var(--color-purple-500)` |
| `--color-purple-300` | `#b794f4`                 |
| `--color-purple-500` | `#805ad5`                 |
| `--color-purple-700` | `#6b46c1`                 |

### Teal

| Property           | Value                   |
| ------------------ | ----------------------- |
| `--color-teal`     | `var(--color-teal-500)` |
| `--color-teal-300` | `#81e6d9`               |
| `--color-teal-500` | `#38b2ac`               |
| `--color-teal-700` | `#2c7a7b`               |

### Yellow

| Property             | Value                     |
| -------------------- | ------------------------- |
| `--color-yellow`     | `var(--color-yellow-500)` |
| `--color-yellow-300` | `#faf089`                 |
| `--color-yellow-500` | `#ecc94b`                 |
| `--color-yellow-700` | `#d69e2e`                 |

### Orange

| Property             | Value                     |
| -------------------- | ------------------------- |
| `--color-orange`     | `var(--color-orange-500)` |
| `--color-orange-300` | `#fbd38d`                 |
| `--color-orange-500` | `#ff9800`                 |
| `--color-orange-700` | `#dd6b20`                 |

### Brown

| Property            | Value                    |
| ------------------- | ------------------------ |
| `--color-brown`     | `var(--color-brown-500)` |
| `--color-brown-300` | `#a1887f`                |
| `--color-brown-500` | `#795548`                |
| `--color-brown-700` | `#5d4037`                |
