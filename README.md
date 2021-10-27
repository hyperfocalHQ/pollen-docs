---
description: Utility-first CSS for the future
---

# Introducing Pollen

Pollen is a standards-driven, utility-first CSS library inspired by [Tailwind](https://tailwindcss.com). It provides a library of [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--\*) that encourage consistency, maintainability, and rapid development. Use it from prototype to production, as a utility-first foundation for your own design system.

### What it looks like

Pollen's low-level variables can be used to build any design. They work anywhere and don't require a buildstep or class naming conventions. They're easy to extend and globally responsive, without introducing preprocessors or new syntax.


{% tabs %}
{% tab title="CSS" %}
```css
.button {
  font-family: var(--font-sans);
  padding: var(--size-2) var(--size-3);
  border-radius: var(--radius-md);
}
```
{% endtab %}

{% tab title="CSS-in-JS" %}
```jsx
const Button = styled.button`
  font-family: var(--font-sans);
  padding: var(--size-2) var(--size-3);
  border-radius: var(--radius-md);
`
```
{% endtab %}

{% tab title="Inline Styles" %}
```markup
<button style="font-family: var(--font-sans); padding: var(--size-2) var(--size-3); border-radius: var(--radius-md);">
  Button
</button>
```
{% endtab %}

{% tab title="Object styles" %}
```jsx
<button styles={{ 
  fontFamily: 'var(--font-sans)',
  padding: 'var(--size-2) var(--size-3)',
  borderRadius: 'var(--radius-md)'
}}>
  Button
</button>
  
```
{% endtab %}
{% endtabs %}

{% embed url="https://codepen.io/madeleineostoja/pen/LYjGjGa" %}

## Who's using Pollen

Pollen is used in production by awesome brands and individuals in projects from small to large-scale. Are you using Pollen? [Open an issue on Github](https://github.com/peppercornstudio/pollen/issues/new) to add your site to the list.

![Corellium](.gitbook/assets/corellium.png)

![Inventia](.gitbook/assets/inventia.png) ![Siesta Campers](.gitbook/assets/siestacampers.png)

![Faethm](.gitbook/assets/faethm.png) ![Madeleine Ostoja](.gitbook/assets/madeleineostoja.png)
