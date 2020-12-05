---
description: Rapid visual prototyping
---

# Colors

| Property group | Applies to |
| :--- | :--- |
| `--color-*` | `color` , `background-color` |

Pollen comes with a robust color pallete to encourage consistency across a project. Using variables like Pollen's ensures there is a single source of truth for colors.

Each color has a family of shades ranging from `300` \(light\) to `700` \(dark\), as well as an extended greyscale. The unsuffixed color \(eg: `--color-red`\) in each family is an alias for median in that family \(eg: `--color-red-500`\).

```css
.alert {
  color: var(--color-red);
}
```

### Greyscale

| Property | Value |
| :--- | :--- |
| `--color-grey` | `var(--color-grey-500)` |
| `--color-grey-100` | `#f7fafc` |
| `--color-grey-300` | `#f4f5f9` |
| `--color-grey-500` | `#8f919b` |
| `--color-grey-700` | `#4a5568` |
| `--color-black` | `#1a202c` |

### Red

| Property | Value |
| :--- | :--- |
| `--color-red` | `var(--color-red-500)` |
| `--color-red-300` | `#fc8181` |
| `--color-red-500` | `#e53e3e` |
| `--color-red-700` | `#c53030` |

### Green

| Variable | Value |
| :--- | :--- |
| `--color-green` | `var(--color-green-500)` |
| `--color-green-300` | `#9ae6b4` |
| `--color-green-500` | `#48bb78` |
| `--color-green-700` | `#2f855a` |

### Blue

| Variable | Value |
| :--- | :--- |
| `--color-blue` | `var(--color-blue-500)` |
| `--color-blue-300` | `#63b3ed` |
| `--color-blue-500` | `#4299e1` |
| `--color-blue-700` | `#3182ce` |

### Pink

| Property | Value |
| :--- | :--- |
| `--color-pink` | `var(--color-pink-500)` |
| `--color-pink-300` | `#fbb6ce` |
| `--color-pink-500` | `#ed64a6` |
| `--color-pink-700` | `#d53f8c` |

### Purple

| Property | Value |
| :--- | :--- |
| `--color-purple` | `var(--color-purple-500)` |
| `--color-purple-300` | `#b794f4` |
| `--color-purple-500` | `#805ad5` |
| `--color-purple-700` | `#6b46c1` |

### Indigo

| Property | Value |
| :--- | :--- |
| `--color-indigo` | `var(--color-indigo-500)` |
| `--color-indigo-300` | `#7f9cf5` |
| `--color-indigo-500` | `#5a67d8` |
| `--color-indigo-700` | `#4c51bf` |

### Teal

| Property | Value |
| :--- | :--- |
| `--color-teal` | `var(--color-teal-500)` |
| `--color-teal-300` | `#81e6d9` |
| `--color-teal-500` | `#38b2ac` |
| `--color-teal-700` | `#2c7a7b` |

### Yellow

| Property | Value |
| :--- | :--- |
| `--color-yellow` | `var(--color-yellow-500)` |
| `--color-yellow-300` | `#faf089` |
| `--color-yellow-500` | `#ecc94b` |
| `--color-yellow-700` | `#d69e2e` |

### Orange

| Property | Value |
| :--- | :--- |
| `--color-orange` | `var(--color-orange-500)` |
| `--color-orange-300` | `#fbd38d` |
| `--color-orange-500` | `#ff9800` |
| `--color-orange-700` | `#dd6b20` |

### Brown

| Property | Value |
| :--- | :--- |
| `--color-brown` | `var(--color-brown-500)` |
| `--color-brown-300` | `#a1887f` |
| `--color-brown-500` | `#795548` |
| `--color-brown-700` | `#5d4037` |

