# Getting started

Since Pollen is built on plain CSS variables, it works everywhere. There's no buildstep or environment requirements. It works in plain CSS, other frameworks, and CSS-in-JS. 

### Installation

Install Pollen from NPM and include it in your project

```bash
npm i pollen-css
```

```javascript
import 'pollen-css';
```

#### Alternatively include from a CDN

You can also link Pollen's CSS directly from the Unpkg CDN

```markup
<link rel="stylesheet" href="https://unpkg.com/pollen-css/pollen.css" />
```

The entire library weighs **under** **1.5kb**, so there's no need to worry about how you bundle or optimise it.

### Usage

Once Pollen is included in your project, you can use its variables _anywhere_ in your styles

```css
.button {
  font: var(--font-sans);
  padding: var(--spacing-1);
  background: var(--color-blue);
  border-radius: var(--radius-2);
  color: var(--color-primary);
}

:root {
  --color-primary: var(--color-blue);
}
```

### Shimming IE

Pollen requires a small shim to work in Internet Explorer, as it doesn't support the CSS variables that the library is built on. 

Enable IE support with the included `shimmie` utility from `pollen-css/utils`

```javascript
import { shimmie } from 'pollen-css/utils';

shimmie();
```

Shimmie will check for support, and if required  dynamically load and apply the excellent [`css-vars-ponfyill`](https://jhildenbiddle.github.io/css-vars-ponyfill/#/) shim with sane configuration.

### Customising Pollen

You can override any variable in Pollen by redefining it. Variables can be redefined in any CSS selector, but to apply globally should be set on the `:root` pseudo element

```css
:root {
  --font-family-sans: 'Inter', sans-serif;
}
```

