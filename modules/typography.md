---
description: Foundations in type
---

# Typography

### Modular Scale

| Property group | Applies to |
| :--- | :--- |
| `--scale-*` | `font-size` |

Pollen provides a robust modular typography scale to encourage consistent typography sizing across an interface. Sizes are set in `rem` units to support proper font scaling, and assume a `16px` root `font-size`.

```css
.heading {
  font-size: var(--scale-4);
}
```

| Property | Value | Equivalent to |
| :--- | :--- | :--- |
| `--scale-000` | `0.75rem` | `12px` |
| `--scale-00` | `0.875rem` | `14px` |
| `--scale-0` | `1rem` | `16px` |
| `--scale-1` | `1.125rem` | `18px` |
| `--scale-2` | `1.25rem` | `20px` |
| `--scale-3` | `1.5rem` | `24px` |
| `--scale-4` | `1.875rem` | `30px` |
| `--scale-5` | `2.25rem` | `36px` |
| `--scale-6` | `3rem` | `48px` |
| `--scale-7` | `3.75rem` | `60px` |
| `--scale-8` | `4.5rem` | `72px` |
| `--scale-9` | `6rem` | `96px` |
| `--scale-10` | `8rem` | `128px` |

### Font Families

| Property group | Applies to |
| :--- | :--- |
| `--font-*` | `font-family` |

Base font stacks as better alternatives to browser defaults, designed for rapid prototyping and to be overridden as your project grows.

```css
body {
  font-family: var(--font-family-sans);
}
```

| Property | Value |
| :--- | :--- |
| `--font-sans` | `system-ui,-apple-system,Segoe UI,Roboto,Noto Sans,Ubuntu,Cantarell,Helvetica Neue` |
| `--font-serif` | `Georgia, Cambria, "Times New Roman", Times, serif` |
| `--font-mono` | `Consolas, Menlo, Monaco, "Liberation Mono", monospace` |

### Weights

| Property group | Applies to |
| :--- | :--- |
| `--font-*` | `font-weight` |

Consistent font weights across an interface

```css
.heading {
  font-weight: var(--font-weight-bold)
}
```

| Property | Value |
| :--- | :--- |
| `--font-light` | `300` |
| `--font-regular` | `400` |
| `--font-medium` | `500` |
| `--font-semibold` | `600` |
| `--font-bold` | `700` |
| `--font-black` | `900` |

### Leading

| Property group | Applies to |
| :--- | :--- |
| `--leading-*` | `line-height` |

Encourage consistent line heights across an interface, applied as unitless values to scale with font size.

```css
body {
  line-height: var(--leading-normal);
}
```

| Property | Value |
| :--- | :--- |
| `--leading-none` | `1` |
| `--leading-xs` | `1.25` |
| `--leading-sm` | `1.275` |
| `--leading-normal` | `1.5` |
| `--leading-lg` | `1.625` |
| `--leading-xl` | `2` |

### Tracking

| Property group | Applies to |
| :--- | :--- |
| `--tracking-*` | `letter-spacing` |

Encourage consistent letter spacing across an interface, applied as `em` units relative to the text's size

```css
.uppercase {
  letter-spacing: var(--tracking-00);
}
```

| Property | Value |
| :--- | :--- |
| `--tracking-000` | `-0.05em` |
| `--tracking-00` | `-0.025em` |
| `--tracking-0` | `0` |
| `--tracking-1` | `0.025em` |
| `--tracking-2` | `0.05em` |
| `--tracking-3` | `0.1em` |

### Measure

| Property group | Applies to |
| :--- | :--- |
| `--measure-*` | `max-width` |

Easy defaults for good legibility in large blocks of text, designed to result in pleasing text measures. Set as `em` units to be relative to the size of the text.

```css
article {
  max-width: var(--measure-normal);
  margin: 0 auto;
}
```

| Property | Value | Measure |
| :--- | :--- | :--- |
| `--measure-narrow` | `20em` | ~45 characters |
| `--measure-normal` | `30em` | ~66 characters |
| `--measure-wide` | `34em` | ~80 characters |

