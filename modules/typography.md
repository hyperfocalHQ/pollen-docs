---
description: Foundations in type
---

# Typography

## Modular Scale

Pollen provides a robust modular typography scale to encourage consistent typography sizing across an interface. Sizes are set in `rem` units to support proper font scaling, and assume a `16px` root `font-size`.

| Property group | Applies to  |
| -------------- | ----------- |
| `--scale-*`    | `font-size` |

```css
.heading {
  font-size: var(--scale-4);
}
```

| Property      | Value      | Equivalent to |
| ------------- | ---------- | ------------- |
| `--scale-000` | `0.75rem`  | `12px`        |
| `--scale-00`  | `0.875rem` | `14px`        |
| `--scale-0`   | `1rem`     | `16px`        |
| `--scale-1`   | `1.125rem` | `18px`        |
| `--scale-2`   | `1.25rem`  | `20px`        |
| `--scale-3`   | `1.5rem`   | `24px`        |
| `--scale-4`   | `1.875rem` | `30px`        |
| `--scale-5`   | `2.25rem`  | `36px`        |
| `--scale-6`   | `3rem`     | `48px`        |
| `--scale-7`   | `3.75rem`  | `60px`        |
| `--scale-8`   | `4.5rem`   | `72px`        |
| `--scale-9`   | `6rem`     | `96px`        |
| `--scale-10`  | `8rem`     | `128px`       |

## Font Families

Base font stacks as better alternatives to browser defaults, designed for rapid prototyping and to be overridden as your project grows.

| Property group | Applies to    |
| -------------- | ------------- |
| `--font-*`     | `font-family` |

```css
body {
  font-family: var(--font-sans);
}
```

| Property       | Value                                                                               |
| -------------- | ----------------------------------------------------------------------------------- |
| `--font-sans`  | `system-ui,-apple-system,Segoe UI,Roboto,Noto Sans,Ubuntu,Cantarell,Helvetica Neue` |
| `--font-serif` | `Georgia, Cambria, "Times New Roman", Times, serif`                                 |
| `--font-mono`  | `Consolas, Menlo, Monaco, "Liberation Mono", monospace`                             |

## Weights

Consistent font weights across an interface

| Property group | Applies to    |
| -------------- | ------------- |
| `--font-*`     | `font-weight` |

```css
.heading {
  font-weight: var(--font-bold)
}
```

| Property           | Value |
| ------------------ | ----- |
| `--font-light`     | `300` |
| `--font-regular`   | `400` |
| `--font-medium`    | `500` |
| `--font-semibold`  | `600` |
| `--font-bold`      | `700` |
| `--font-extrabold` | `800` |
| `--font-black`     | `900` |

## Line Height

Encourage consistent line heights across an interface, applied as unitless values to scale with font size.

| Property group | Applies to    |
| -------------- | ------------- |
| `--line-*`     | `line-height` |

```css
body {
  line-height: var(--line-md);
}
```

| Property      | Value   |
| ------------- | ------- |
| `--line-none` | `1`     |
| `--line-xs`   | `1.25`  |
| `--line-sm`   | `1.275` |
| `--line-md`   | `1.5`   |
| `--line-lg`   | `1.625` |
| `--line-xl`   | `2`     |

## Letter Spacing

Encourage consistent letter spacing across an interface, applied as `em` units relative to the text's size

| Property group | Applies to       |
| -------------- | ---------------- |
| `--letter-*`   | `letter-spacing` |

```css
.uppercase {
  letter-spacing: var(--letter-xs);
}
```

| Property        | Value      |
| --------------- | ---------- |
| `--letter-xs`   | `-0.05em`  |
| `--letter-sm`   | `-0.025em` |
| `--letter-none` | `0`        |
| `--letter-lg`   | `0.025em`  |
| `--letter-xl`   | `0.05em`   |

## Prose Width

Max-widths optimised for legibility of large blocks of text, based on the font and font-size of content.

| Property group | Applies to  |
| -------------- | ----------- |
| `--prose-*`    | `max-width` |

```css
article {
  max-width: var(--prose-normal);
  margin: 0 auto;
}
```

| Property     | Value  | Measure    |
| ------------ | ------ | ---------- |
| `--prose-xs` | `45ch` | 45 letters |
| `--prose-sm` | `55ch` | 55 letters |
| `--prose-md` | `65ch` | 65 letters |
| `--prose-lg` | `75ch` | 75 letters |
| `--prose-xl` | `85ch` | 85 letters |
