---
description: Consistency across UI and motion
---

# UI

## Radius

Consistent edge radiuses throughout an interface.

| Property group | Applies to      |
| -------------- | --------------- |
| `--radius-*`   | `border-radius` |

![](../.gitbook/assets/borders.svg)

```css
.button {
  border-radius: var(--radius-md);
}
```

| Property        | Value    |
| --------------- | -------- |
| `--radius-xs`   | `3px`    |
| `--radius-sm`   | `6px`    |
| `--radius-md`   | `8px`    |
| `--radius-lg`   | `12px`   |
| `--radius-xl`   | `16px`   |
| `--radius-100`  | `100%`   |
| `--radius-full` | `9999px` |

## Shadow

Box shadows for creating realistic elevation in 3d space.

| Property group | Applies to   |
| -------------- | ------------ |
| `--shadow-*`   | `box-shadow` |

![](../.gitbook/assets/Shadows.png)

```css
.card {
  box-shadow: var(--shadow-sm);
}
```

| Property      | Value                                                                       |
| ------------- | --------------------------------------------------------------------------- |
| `--shadow-xs` | `0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06)`           |
| `--shadow-sm` | `0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06)`     |
| `--shadow-md` | `0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05)`   |
| `--shadow-lg` | `0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04)` |
| `--shadow-xl` | `0 25px 50px -12px rgba(0, 0, 0, 0.25)`                                     |

## Blur

Backdrop blur effects for giving a sense of depth to an interface

| Property Group | Applies to        |
| -------------- | ----------------- |
| `--blur-*`     | `backdrop-filter` |

![](<../.gitbook/assets/blur (1).jpg>)

```css
.overlay {
  backdrop-filter: var(--blur-md);
}
```

| Property    | Value        |
| ----------- | ------------ |
| `--blur-xs` | `blur(4px)`  |
| `--blur-sm` | `blur(8px)`  |
| `--blur-md` | `blur(16px`) |
| `--blur-lg` | `blur(24px)` |
| `--blur-xl` | `blur(40px)` |

## Easing

Easing functions for realistic movement in transitions and animations

| Property Group | Applies to                |
| -------------- | ------------------------- |
| `--ease-*`     | `transition`, `animation` |

```css
.animated {
  transition: all 300ms var(--ease-in-cubic);
}
```

<figure><img src="../.gitbook/assets/Screen Shot 2022-09-17 at 10.46.29 PM.png" alt=""><figcaption></figcaption></figure>

| Property              | Value                                     |
| --------------------- | ----------------------------------------- |
| `--ease-in-sine`      | `cubic-bezier(0.47, 0, 0.745, 0.715)`     |
| `--ease-out-sine`     | `cubic-bezier(0.39, 0.575, 0.565, 1)`     |
| `--ease-in-out-sine`  | `cubic-bezier(0.445, 0.05, 0.55, 0.95)`   |
| `--ease-in-quad`      | `cubic-bezier(0.55, 0.085, 0.68, 0.53)`   |
| `--ease-out-quad`     | `cubic-bezier(0.25, 0.46, 0.45, 0.94)`    |
| `--ease-in-out-quad`  | `cubic-bezier(0.455, 0.03, 0.515, 0.955)` |
| `--ease-in-cubic`     | `cubic-bezier(0.55, 0.055, 0.675, 0.19)`  |
| `--ease-out-cubic`    | `cubic-bezier(0.215, 0.61, 0.355, 1)`     |
| `--ease-in-out-cubic` | `cubic-bezier(0.645, 0.045, 0.355, 1)`    |
| `--ease-in-quart`     | `cubic-bezier(0.895, 0.03, 0.685, 0.22)`  |
| `--ease-out-quart`    | `cubic-bezier(0.165, 0.84, 0.44, 1)`      |
| `--ease-in-out-quart` | `cubic-bezier(0.77, 0, 0.175, 1)`         |
| `--ease-in-quint`     | `cubic-bezier(0.755, 0.05, 0.855, 0.06)`  |
| `--ease-out-quint`    | `cubic-bezier(0.23, 1, 0.32, 1)`          |
| `--ease-in-out-quint` | `cubic-bezier(0.86, 0, 0.07, 1)`          |
| `--ease-in-expo`      | `cubic-bezier(0.95, 0.05, 0.795, 0.035)`  |
| `--ease-out-expo`     | `cubic-bezier(0.19, 1, 0.22, 1)`\`        |
| `--ease-in-out-expo`  | `cubic-bezier(1, 0, 0, 1)`                |
| `--ease-in-circ`      | `cubic-bezier(0.6, 0.04, 0.98, 0.335)`    |
| `--ease-out-circ`     | `cubic-bezier(0.075, 0.82, 0.165, 1)`     |
| `--ease-in-out-circ`  | `cubic-bezier(0.785, 0.135, 0.15, 0.86)`  |
| `--ease-in-back`      | `cubic-bezier(0.6, -0.28, 0.735, 0.045)`  |
| `--ease-out-back`     | `cubic-bezier(0.175, 0.885, 0.32, 1.275)` |
| `--ease-in-out-back`  | `cubic-bezier(0.68, -0.55, 0.265, 1.55)`  |

## Layers

Consistent layering throughout an interface

| Property group | Applies to |
| -------------- | ---------- |
| `--layer-*`    | `z-index`  |

```css
.elevated {
  position: relative;
  z-index: var(--layer-1);
}
```

| Property        | Value        |
| --------------- | ------------ |
| `--layer-below` | `-1`         |
| `--layer-1`     | `10`         |
| `--layer-2`     | `20`         |
| `--layer-3`     | `30`         |
| `--layer-4`     | `40`         |
| `--layer-5`     | `50`         |
| `--layer-top`   | `2147483647` |
