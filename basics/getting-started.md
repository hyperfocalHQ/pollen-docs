# Getting started

Since Pollen is just CSS variables, it works everywhere without any preprocessor or environment requirements.

### Installation

Install Pollen from NPM and include its CSS in your project

```bash
npm i pollen-css
```

{% tabs %}
{% tab title="Module import" %}
```javascript
import 'pollen-css';
```

> Requires CSS support in your bundler (eg: Webpack, Rollup, etc)
{% endtab %}

{% tab title="CSS import" %}
{% code title="With bundler" %}
```css
@import "pollen-ss";
```
{% endcode %}

{% code title="Plain import" %}
```css
@import "/node_modules/pollen-css/pollen.css";
```
{% endcode %}

> If linking directly to `node_modules` they need to be shipped with your frontend. Consider either [generating your own bundle](getting-started.md#configuration) or pulling from a CDN instead (see below)
{% endtab %}

{% tab title="HTML Link" %}
```markup
<link rel="stylesheet" href="/node_modules/pollen-css/pollen.css" />
```

> Linking directly to `pollen.css` in HTML means your `node_modules` needs to be shipped with your frontend. Consider either [generating your own bundle](getting-started.md#configuration) or pulling from a CDN instead (see below)
{% endtab %}
{% endtabs %}

#### Including from a CDN

You can also link Pollen's CSS directly from the Unpkg CDN

```html
<link rel="stylesheet" href="https://unpkg.com/pollen-css/pollen.css" />
```

Once Pollen is included in your project, you can use its variables anywhere

### Configuration

Pollen comes with a robust set of low-level defaults for building sophisticated designs. But every aspect can be easily customised, extended, or stripped out with the `pollen` command line build tool. Instead of importing the default `pollen.css` file, create a `pollen.config.js` config file in the root of your project and run `pollen` to generate your own custom design system. Then import the generated CSS file as you normally would.

Read more in [configuration](configuration/ "mention").

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
    // Or your custom Pollen bundle
    "./node_modules/pollen-css/pollen.css", 
  ],
  // Use Pollen's inbuilt variable ordering
  "cssvar.disableSort": true, 
   // Add support for autocomplete in other file types
  "cssvar.extensions": ["css", "html", "jsx", "tsx"] 
}
```
{% endcode %}
