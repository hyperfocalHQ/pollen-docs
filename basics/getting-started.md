# Getting started

Since Pollen is just CSS variables, it works everywhere without any configuration needed. There's no buildstep, preprocessor, or environment requirements. It weighs less than 1kb.

## Installation & Usage

Install Pollen from NPM and include it in your project

```bash
npm i pollen-css
```

```javascript
import 'pollen-css';
```

#### Alternatively include from a CDN

You can also link Pollen's CSS directly from the Unpkg CDN

```html
<link rel="stylesheet" href="https://unpkg.com/pollen-css/pollen.css" />
```

Once Pollen is included in your project, you can use its variables anywhere

### Configuration

### Addons

Pollen comes with a robust set of low-level defaults for building sophisticated designs. But every aspect can be easily customised and extended with the `pollen` command line build tool. Instead of importing the default `pollen.css` file, create a `pollen.config.js` config file in the root of your project and run `pollen` to generate your own custom design system. Then import the generated CSS file as you normally would.

Pollen comes with several optional [addons](getting-started.md#undefined) in addition to its core modules. Include them in your project by importing their CSS file from `pollen-css/addons/{addon}.css`

Read more in [configuration](configuration/ "mention")

```javascript
import 'pollen-css'
import 'pollen-css/addons/grid.css'
```

{% code title="pollen.config.js" %}
```javascript
module.exports = () => ({
  modules: {
    colors: true,
    grid: true
  }
});
```
{% endcode %}

### IE Support

Pollen requires a small shim to work in Internet Explorer 11 and below, as it doesn't support the CSS variables that the library is built on. Enable IE support with the included `shimmie` utility from `pollen-css/utils`

```javascript
import { shimmie } from 'pollen-css/utils';

shimmie();
```

Shimmie will check for support, and if required dynamically load and apply the excellent [`css-vars-ponfyill`](https://jhildenbiddle.github.io/css-vars-ponyfill/#/) shim with sane configuration.

## Editor Integration

### VS Code

Enable intellisense autocompletion for Pollen in VS Code by installing the [CSS Var Complete](https://marketplace.visualstudio.com/items?itemName=phoenisx.cssvar) extension and adding Pollen's CSS in a `.vscode/settings.json` file in the root of your project, along with some optional additional configuration.

If you have [configured a custom Pollen bundle](configuration/) make sure you add the output CSS file to the `cssvar.files` array instead of the default `pollen.css` bundle.

{% code title=".vscode/settings.json" %}
```json
{
  "cssvar.files": [
    "./node_modules/pollen-css/pollen.css", // Or your custom Pollen bundle
  ],
  // Use Pollen's inbuilt variable ordering
  "cssvar.disableSort": true,
  // Add support for autocomplete in other file types
  "cssvar.extensions": ["css", "html", "jsx", "tsx"]
}
```
{% endcode %}
