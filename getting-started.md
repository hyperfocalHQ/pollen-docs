# Getting started

Since Pollen is built on plain CSS variables, it works everywhere. There's no buildstep, preprocessor, or environment requirements.

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

### Usage

Once Pollen is included in your project, you can use its variables anywhere in your styles

```css
.button {
  font-family: var(--font-sans);
  padding: var(--size-2) var(--size-3);
  border-radius: var(--radius);
  background: var(--color-primary);
  color: white;
}
```

### Shimming IE

Pollen requires a small shim to work in Internet Explorer 11 and below, as it doesn't support the CSS variables that the library is built on.

Enable IE support with the included `shimmie` utility from `pollen-css/utils`

```javascript
import { shimmie } from 'pollen-css/utils';

shimmie();
```

Shimmie will check for support, and if required dynamically load and apply the excellent [`css-vars-ponfyill`](https://jhildenbiddle.github.io/css-vars-ponyfill/#/) shim with sane configuration.

### Editor Support

#### VS Code

Enable intellisense autocompletion for Pollen in VS Code by installing the [CSS Var Complete](https://marketplace.visualstudio.com/items?itemName=phoenisx.cssvar) extension and adding Pollen's CSS to its settings in a `.vscode/settings.json` file in the root of your project, along with some optional additional configuration.

{% code title=".vscode/settings.json" %}
```javascript
{
  // Add Pollen autocomplete
  "cssvar.files": [
    "./node_modules/pollen-css/pollen.css",
    // "./src/styles/my-custom-variables.css
  ],
  // Use Pollen's inbuilt variable ordering
  "cssvar.unstable": ["no_sort"],
  // Add support for autocomplete in other file types
  "cssvar.extensions": ["css", "html", "jsx", "tsx"]
}
```
{% endcode %}
