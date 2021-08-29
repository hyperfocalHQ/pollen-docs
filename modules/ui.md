---
description: Consistency across UI and motion
---

# UI

### Elevation

| Property group | Applies to |
| :--- | :--- |
| `--elevation-*` | `box-shadow` |

Box shadows for creating realistic elevation in 3d space.

```css
.card {
  box-shadow: var(--elevation-1);
}
```

| Property | Value |
| :--- | :--- |
| `--elevation-1` | `0 1px 2px 0 rgba(0, 0, 0, 0.05)` |
| `--elevation-2` | `0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06)` |
| `--elevation-3` | `0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06)` |
| `--elevation-4` | `0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05)` |
| `--elevation-5` | `0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04)` |
| `--elevation-6` | `0 25px 50px -12px rgba(0, 0, 0, 0.25)` |

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

Consistent edge radiuses throughout an interface.

```css
.button {
  border-radius: var(--radius-2);
}
```

| Property | Value |
| :--- | :--- |
| `--radius-none` | `0px;` |
| `--radius-sm` | `0.125rem` |
| `--radius` | `0.25rem` |
| `--radius-md` | `0.375rem` |
| `--radius-lg` | `0.5rem` |
| `--radius-xl` | `0.75rem` |
| `--radius-2xl` | `1rem` |
| `--radius-3xl` | `1.5rem` |
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
| `--layer-top` | `2147483647` |

