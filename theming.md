# Theming

Pollen is built on [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/--*), a new web specification that allows us to define custom CSS properties that can be used anywhere in your project. Since they are defined globally and represent a single source of truth, variables allow us to do things not previously possible in CSS.

### Global responsiveness

Pollen’s CSS variables can be changed inside media queries, to update their value across a project. Redefine a variable on `:root` in a media query. All instances of that variable will then update when the media query is triggered.

```css
@media (min-width: 45em) {
  :root {
    --body-font-size: var(--scale-1);
  }
}
```

### Interacting with JS

CSS variables are also accessible in JavaScript, which allows you to accomplish things that were previously very complicated, like dynamically applying style themes. By updating a few key variables based on user input, you can reskin an entire interface.

Update CSS variables in JS by using the `setProperty` method on the document root’s style property.

```javascript
document.documentElement.style.setProperty(
  `--font-family-sans`,
  `'Garamond', serif`
);
```

You can also alias variables to other variables, this is useful for using a consistent property throughout your codebase that can be dynamically updated without losing meaning

```javascript
document.documentElement.style.setProperty(
  `--color-primary`,
  `var(--color-blue)`
);
```

