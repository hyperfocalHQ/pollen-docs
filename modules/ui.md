---
description: Consistency across UI and motion
---

# UI

### Elevation

| Property group | Applies to |
| :--- | :--- |
| `--elevation-*` | `box-shadow` |

Box shadows for creating realistic elevation in 3d space. Inspired by [Material Design guidelines on depth](https://material.io/design/environment/elevation.html)

```css
.card {
  box-shadow: var(--elevation-1);
}
```

| Property | Value |
| :--- | :--- |
| `--elevation-1` | `0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.2), 0 1px 5px 0 rgba(0, 0, 0, 0.12)` |
| `--elevation-2` | `0 3px 4px 0 rgba(0, 0, 0, 0.14), 0 3px 3px -2px rgba(0, 0, 0, 0.2), 0 1px 8px 0 rgba(0, 0, 0, 0.12)` |
| `--elevation-3` | `0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12), 0 2px 4px -1px rgba(0, 0, 0, 0.2)` |
| `--elevation-4` | `0 6px 10px 0 rgba(0, 0, 0, 0.14), 0 1px 18px 0 rgba(0, 0, 0, 0.12), 0 3px 5px -1px rgba(0, 0, 0, 0.2)` |
| `--elevation-5` | `0 8px 10px 1px rgba(0, 0, 0, 0.14), 0 3px 14px 2px rgba(0, 0, 0, 0.12), 0 5px 5px -3px rgba(0, 0, 0, 0.2)` |
| `--elevation-6` | `0 16px 24px 2px rgba(0, 0, 0, 0.14), 0 6px 30px 5px rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2)` |

### Easing

| Property group | Applies to |
| :--- | :--- |
| `--easing-*` | `transition`  and  `animation` |

Easing functions for realistic movement in transitions and animations. Inspired by the Material Design guidelines on motion.

```css
.animated {
  transition: all 300ms var(--easing-standard);
}
```

| Property | Value |
| :--- | :--- |
| `--easing-standard` | `cubic-bezier(0.4, 0, 0.2, 1)` |
| `--easing-accelerate` | `cubic-bezier(0.4, 0, 1, 1)` |
| `--easing-decelerate` | `cubic-bezier(0, 0, 0.2, 1)` |

### Radius

| Property group | Applies to |
| :--- | :--- |
| `--radius-*` | `border-radius` |

Consistent edge radiuses throughout an interface, applied as `em` units to be relative to the content of the item

```css
.button {
  border-radius: var(--radius-2);
}
```

| Property | Value |
| :--- | :--- |
| `--radius-1` | `0.2em` |
| `--radius-2` | `0.375em` |
| `--radius-3` | `0.5em` |
| `--radius-4` | `0.8em` |
| `--radius-5` | `1em` |
| `--radius-6` | `1.25em` |
| `--radius-round` | `9999px` |

### Layers

| Property group | Applies to |
| :--- | :--- |
| `--layer-*` | `z-index` |

Consistent layering throughout an interface

```css
.elevated {
  position: relative;
  z-index: var(--layer-1);
}
```

| Property | Value |
| :--- | :--- |
| `--layer-1` | `10` |
| `--layer-2` | `20` |
| `--layer-3` | `30` |
| `--layer-4` | `40` |
| `--layer-5` | `50` |
| `--layer-6` | `60` |
| `--layer-top` | `2147483647` |

