# Getting started

Since Pollen is built on plain CSS variables, it works everywhere. There's no buildstep or environment requirements. It works in plain CSS, other frameworks, and CSS-in-JS.

## Installation

Install Pollen from NPM and include it in your project

```bash
npm i pollen-css
```

```javascript
import 'pollen-css';
```

### Alternatively include from a CDN

You can also link Pollen's CSS directly from the Unpkg CDN

```markup
<link rel="stylesheet" href="https://unpkg.com/pollen-css/pollen.css" />
```

The entire library weighs **under** **1.5kb**, so there's no need to worry about how you bundle or optimise it.

## Usage

Once Pollen is included in your project, you can use its variables anywhere in your styles

```css
.button {
  font: var(--font-sans);
  padding: var(--size-1);
  border-radius: var(--radius-2);
  color: var(--color-primary);
}

:root {
  --color-primary: var(--color-blue);
}
```

## Shimming IE

Pollen requires a small shim to work in Internet Explorer, as it doesn't support the CSS variables that the library is built on.

Enable IE support with the included `shimmie` utility from `pollen-css/utils`

```javascript
import { shimmie } from 'pollen-css/utils';

shimmie();
```

Shimmie will check for support, and if required dynamically load and apply the excellent [`css-vars-ponfyill`](https://jhildenbiddle.github.io/css-vars-ponyfill/#/) shim with sane configuration.

## Editor Support

For autocomplete support of all of Pollen's variables in VS Code:

1. Install the [CSS Var Complete](https://marketplace.visualstudio.com/items?itemName=phoenisx.cssvar) extension
2. Add Pollen to the extension's file settings in `.vscode/settings.json`
3. If you've [extended Pollen](theming.md) make sure you also include your variables stylesheet
4. If you're using CSS-in-JS make sure you add `javascript`/`javascriptreact`/`typescriptreact` file support to the extension's settings

{% code title=".vscode/settings.json" %}
```javascript
{
  "cssvar.files": [
    "./node_modules/pollen-css/pollen.css",
    "./styles/variables.css" // Your theme file
  ],
  
  // CSS-in-JS support
  "cssvar.extensions": ["css", "javascript", "typescriptreact"] 
}
```
{% endcode %}

Autocomplete will then be available for all properties. Intellisense will trigger simply with `--`, no need to also add `var(`.

