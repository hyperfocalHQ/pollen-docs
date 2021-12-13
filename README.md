---
description: Utility-first CSS for the future
cover: .gitbook/assets/cover wide.jpg
coverY: 19.899888765294783
---

# Introducing Pollen

![](<.gitbook/assets/cover wide.jpg>)

Pollen is a standards-driven, utility-first CSS library inspired by [Tailwind](https://tailwindcss.com). It generates a configurable collection of [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--\*) that can be used anywhere to encourage consistency, maintainability, and rapid development. Made and maintained with ❤️ by the fine people at [Bokeh](https://heybokeh.com).

### What it looks like

Pollen's low-level variables can be used to build any design. They're easy to customise and extend, and they're globally responsive. They don't require preprocessors, class naming conventions, or any new non-standard syntax

{% tabs %}
{% tab title="CSS" %}
```css
.button {
   font-family: var(--font-sans);
   font-size: var(--scale-00);
   font-weight: var(--weight-medium); 
   line-height: var(--line-none);
   padding: var(--size-3) var(--size-5);
   background: var(--color-blue);
   border-radius: var(--radius-xs);
   color: white;
}
```
{% endtab %}

{% tab title="CSS-in-JS" %}
```jsx
const Button = styled.button`
   font-family: var(--font-sans);
   font-size: var(--scale-00);
   font-weight: var(--weight-medium); 
   line-height: var(--line-none);
   padding: var(--size-3) var(--size-5);
   background: var(--color-blue);
   border-radius: var(--radius-xs);
   color: white;
`
```
{% endtab %}

{% tab title="Object styles" %}
```jsx
<button styles={{ 
   fontFamily: 'var(--font-sans)',
   fontSize: 'var(--scale-00)',
   fontWeight: 'var(--weight-medium)',
   lineHeight: 'var(--line-none)',
   padding: 'var(--size-3) var(--size-5)',
   background: 'var(--color-blue)',
   borderRadius: 'var(--radius-xs)'
   color: 'white'
}}>
  Button
</button>
  
```
{% endtab %}

{% tab title="Inline Styles" %}
```markup
<button style="font-family: var(--font-sans); font-size: var(--scale-00); font-weight: var(--weight-medium);  line-height: var(--line-none); padding: var(--size-3) var(--size-5); background: var(--color-blue); border-radius: var(--radius-xs); color: white;">
  Button
</button>
```
{% endtab %}
{% endtabs %}

{% embed url="https://codepen.io/madeleineostoja/pen/LYjGjGa" %}

## Who's using Pollen

Pollen is used extensively in production and actively maintained by the photo nerds [Bokeh](https://heybokeh.com). It's also used by many other awesome teams in projects from small to large-scale. Are you using Pollen? [Open an issue on Github](https://github.com/peppercornstudio/pollen/issues/new) to add your site to the list.

![Corellium](.gitbook/assets/corellium.png) ![Bokeh](<.gitbook/assets/Screen Shot 2021-11-14 at 11.27.34 AM.png>)

![Inventia](.gitbook/assets/inventia.png) ![Siesta Campers](.gitbook/assets/siestacampers.png)

![Faethm](.gitbook/assets/faethm.png) ![Madeleine Ostoja](.gitbook/assets/madeleineostoja.png)
