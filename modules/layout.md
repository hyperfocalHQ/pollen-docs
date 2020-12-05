---
description: Structural consistency
---

# Layout

### Size Scale

| Property group | Applies to |
| :--- | :--- |
| `--spacing-*` | Sizing properties \(`margin`, `padding`, `height`, etc\) |

Encourage consistent spacing throughout an interface

```css
section {
  margin-top: var(--spacing-5);
}
```

| Property | Value |
| :--- | :--- |
| `--spacing-000` | `8px` |
| `--spacing-00` | `12px` |
| `--spacing-0` | `16px` |
| `--spacing-1` | `20px` |
| `--spacing-2` | `32px` |
| `--spacing-3` | `48px` |
| `--spacing-4` | `64px` |
| `--spacing-5` | `96px` |
| `--spacing-6` | `128px` |
| `--spacing-7` | `160px` |
| `--spacing-8` | `192px` |
| `--spacing-9` | `224px` |
| `--spacing-10` | `256px` |
| `--spacing-11` | `512px` |
| `--spacing-12` | `768px` |

### Widths

| Property group | Applies to |
| :--- | :--- |
| `--width-*` | `max-width` |

Encourage consistent widths throughout an interface

```css
.page-container {
  max-width: var(--width-11);
  margin: 0 auto;
}
```

| Property | Value |
| :--- | :--- |
| `--width-1` | `320px` |
| `--width-2` | `396px` |
| `--width-3` | `448px` |
| `--width-4` | `512px` |
| `--width-5` | `576px` |
| `--width-6` | `672px` |
| `--width-7` | `768px` |
| `--width-8` | `896px` |
| `--width-9` | `1024px` |
| `--width-10` | `1152px` |
| `--width-11` | `1280px` |
| `--width-12` | `1440px` |

### Gutters & Offsets

| Property group | Applies to |
| :--- | :--- |
| `--gap-*` | `grid-gap` and `padding`/`margin`  |

Encourage consistent gaps in grids, either with [CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/grid) or [flexbox-based grids](https://docs.satchel.style/grids#flexgrid-gutter)

```css
.page-container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-gap: var(--gap-2);
}
```

| Property | Value |
| :--- | :--- |
| `--gap-00` | `12px` |
| `--gap-0` | `16px` |
| `--gap-1` | `24px` |
| `--gap-2` | `36px` |
| `--gap-3` | `48px` |
| `--gap-4` | `64px` |
| `--gap-5` | `96px` |
| `--gap-6` | `128px` |

#### Offsets

| Property group | Applies to |
| :--- | :--- |
| `--gap-offset-*` | `margin` |

Pollen also includes shortcuts for gap offsets, for using on negative margins on the containers of flex-based grid layouts

```css
.container {
  display: flex;
  flex-wrap: wrap;
  margin: var(--gap-offset-2);
}

.inner {
  flex-basis: 50%;
  padding: var(--gap-2);
}
```

| Property | Value |
| :--- | :--- |
| `--gap-offset-00` | `calc(0px - var(--gap-00))` |
| `--gap-offset-0` | `calc(0px - var(--gap-0))` |
| `--gap-offset-1` | `calc(0px - var(--gap-1))` |
| `--gap-offset-2` | `calc(0px - var(--gap-2))` |
| `--gap-offset-3` | `calc(0px - var(--gap-3))` |
| `--gap-offset-4` | `calc(0px - var(--gap-4))` |
| `--gap-offset-5` | `calc(0px - var(--gap-5))` |
| `--gap-offset-6` | `calc(0px - var(--gap-6))` |

