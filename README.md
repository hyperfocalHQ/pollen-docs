---
description: Functional CSS for the future
---

# Introducing Pollen

Pollen is a collection of [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) designed for rapid prototyping, consistent styling, and as a [utility-first](https://frontstuff.io/in-defense-of-utility-first-css) foundation for your own design systems. 

### What it looks like

Pollen has no buildstep, class naming conventions, or framework gotchas. It works in stylesheets, inline styles, and CSS-in-JS.

```css
.button {
  font: var(--font-sans);
  padding: var(--spacing-1);
  background: var(--color-blue);
  color: white;
  border-radius: var(--radius-2);
  box-shadow: var(--elevation-1);
  transition: background 150ms var(--easing-standard);
}
```

### Modules

* [Typography system](modules/typography.md)
* [Color palette](modules/colors.md)
* [Layout scales](modules/layout.md)
* [UI library](modules/layout.md)

{% hint style="info" %}
### **Love Pollen? Try Satchel 🎒**

Satchel is a lightweight library of CSS-in-JS utilities that makes development easier.  
**Get Satchel 👉** [**satchel.style**](https://satchel.style)\*\*\*\*
{% endhint %}

