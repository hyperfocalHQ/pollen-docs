---
description: Foundations in type
---

# Typography

## Modular Scale

Pollen provides a robust modular typography scale to encourage consistent typography sizing across an interface. Sizes are set in `rem` units to support proper font scaling, and assume a `16px` root `font-size`.

| Property group | Applies to  |
| -------------- | ----------- |
| `--scale-*`    | `font-size` |

![](<../.gitbook/assets/modular scale 2.svg>)

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

## Fluid Modular Scale

In addition to the standard modular typographic scale above, Pollen also comes with a fluid scale that tweens between steps on the scale as screen width changes. Its built with Pollen's own [fluid.md](../utils/fluid.md "mention") utility, which generates complex CSS `clamp()` functions based on screen width bounds.

Each fluid font size resizes between a min and max size, starting at mobile screen sizes (`480px`) and ending at normal desktop screen sizes (`1280px`).

| Property group    | Applies to  |
| ----------------- | ----------- |
| `--scale-fluid-*` | `font-size` |

```css
.heading {
  font-size: var(--scale-fluid-5);
}
```

| Property            | Value                                         | Range                   |
| ------------------- | --------------------------------------------- | ----------------------- |
| `--scale-fluid-000` | `clamp(0.625rem, 0.55rem + 0.25vw, 0.75rem)`  | `0.625rem` -> `0.75rem` |
| `--scale-fluid-00`  | `clamp(0.75rem, 0.675rem + 0.25vw, 0.875rem)` | `0.75rem` -> `0.875rem` |
| `--scale-fluid-0`   | `clamp(0.875rem, 0.8rem + 0.25vw, 1rem)`      | `0.875rem` -> `1rem`    |
| `--scale-fluid-1`   | `clamp(1rem, 0.925rem + 0.25vw, 1.125rem)`    | `1rem` -> `1.125rem`    |
| `--scale-fluid-2`   | `clamp(1.125rem, 1.05rem + 0.25vw, 1.25rem)`  | `1.125rem` -> `1.25rem` |
| `--scale-fluid-3`   | `clamp(1.8125rem, 2rem + -0.625vw, 1.5rem)`   | `1.8125rem` -> `1.5rem` |
| `--scale-fluid-4`   | `clamp(1.5rem, 1.275rem + 0.75vw, 1.875rem)`  | `1.5rem` -> `1.875rem`  |
| `--scale-fluid-5`   | `clamp(1.875rem, 1.65rem + 0.75vw, 2.25rem)`  | `1.875rem` -> `2.25rem` |
| `--scale-fluid-6`   | `clamp(2.25rem, 1.8rem + 1.5vw, 3rem)`        | `2.25rem` -> `3rem`     |
| `--scale-fluid-7`   | `clamp(3rem, 2.55rem + 1.5vw, 3.75rem)`       | `3rem` -> `3.75rem`     |
| `--scale-fluid-8`   | `clamp(3.75rem, 3.3rem + 1.5vw, 4.5rem)`      | `3.75rem` -> `4.5rem`   |
| `--scale-fluid-9`   | `clamp(4.5rem, 3.6rem + 3vw, 6rem)`           | `4.5rem` -> `6rem`      |
| `--scale-fluid-10`  | `clamp(6rem, 4.8rem + 4vw, 8rem)`             | `6rem` -> `8rem`        |

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

## Font Weights

Consistent font weights across an interface

```css
.heading {
  font-weight: var(--weight-bold)
}
```

| Property group | Applies to    |
| -------------- | ------------- |
| `--weight-*`   | `font-weight` |

| Property             | Value |
| -------------------- | ----- |
| `--weight-light`     | `300` |
| `--weight-regular`   | `400` |
| `--weight-medium`    | `500` |
| `--weight-semibold`  | `600` |
| `--weight-bold`      | `700` |
| `--weight-extrabold` | `800` |
| `--weight-black`     | `900` |

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
