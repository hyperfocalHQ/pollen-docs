# Configuration

While Pollen provides a default bundle of robust, useful low-level variables to build your project with (under `pollen-css/pollen.css`). It also comes with a build tool to generate your own custom design system instead.

Start by creating a config file in the root of your project that exports either a function or an object. See the full list of configuration options below.

The config file can be in CommonJS or ESM format, and will automatically be loaded with any of the following filenames:

* `pollen.config.{js|cjs|mjs}`
* `pollenrc.{js|cjs|mjs}`

{% code title="pollen.config.js" %}
```javascript
module.exports = {
  // Config options
}
```
{% endcode %}

Once you have a configuration file, run the included `pollen` CLI tool. Either install `pollen-css` globally, or run the tool in an NPM script or with `npx`.

{% tabs %}
{% tab title="Global install" %}
```
$ npm i -g pollen-css
$ pollen
```
{% endtab %}

{% tab title="Local install" %}
```
npm i pollen-css
npx pollen
```
{% endtab %}
{% endtabs %}

Then import/link to the output stylesheet in your project instead of the default Pollen export

{% tabs %}
{% tab title="Javascript" %}
```javascript
import './pollen.css'
```
{% endtab %}

{% tab title="HTML" %}
```html
<link rel="stylesheet" href="/pollen.css" />
```
{% endtab %}
{% endtabs %}

#### Managing Pollen builds in production

Since the output CSS is a generated file, we recommend excluding this output from version control like git and running the `pollen` build tool along with the rest of your build pipeline, in a CI step or similar. You can do this with a `prebuild` script in `package.json`

{% code title="package.json" %}
```json
{
  "scripts": {
    "prebuild": "pollen"
  }
}
```
{% endcode %}

### Config options

<table><thead><tr><th width="161">Option</th><th width="155.7450980392157">Default</th><th>Description</th></tr></thead><tbody><tr><td><code>output</code></td><td><code>./pollen.css</code></td><td>File path of the generated Pollen stylesheet and optional JSON schema</td></tr><tr><td><code>selector</code></td><td><code>:root</code></td><td>CSS selector to scope Pollen's variables to</td></tr><tr><td><code>modules</code></td><td>Pollen default values</td><td>Pollen module configuration, see <a data-mention href="configuring-modules.md">configuring-modules.md</a></td></tr><tr><td><code>media</code></td><td><code>undefined</code></td><td>Media queries, see <a data-mention href="queries.md">queries.md</a></td></tr><tr><td><code>supports</code></td><td><code>undefined</code></td><td>Supports queries, see <a data-mention href="queries.md">queries.md</a></td></tr></tbody></table>

```javascript
module.exports = {
  output: './styles/pollen.css',
  modules: {
    // Module config
  }
}
```

### CLI options

| Option           | Default                          | Description                              |
| ---------------- | -------------------------------- | ---------------------------------------- |
| `-c`, `--config` | `./pollen.config.js`             | Path to your Pollen config file          |
| `-o`, `--output` | Value of `output` in config file | File path to generated Pollen stylesheet |

```
pollen -c ./pollen-dev.config.js -o ./styles/pollen-dev.css
```

### Exporting a JSON schema

The `output` option in Pollen's config also accepts an object with a `json` field, which will generate a JSON schema of your design system. This is useful for internal documentation if your [module configuration](configuring-modules.md) differs significantly from Pollen's defaults, which are documented here.

```javascript
module.exports = {
  output: {
    css: './styles/pollen.css',
    json: './docs/pollen.json'
  }
}
```

### Changing the CSS selector

By default Pollen scopes all its variables to `:root`. This is generally what you want, it will make your style variables available globally through your site, polyfill-able for IE11, and easy to reactively modify with media queries and javascript.&#x20;

However you can change this with the `selector` option in Pollen's config, a potential use-case is to make it `:host` for a shadow DOM, or a HTML element if you want to scope Pollen to part of your project

```javascript
module.exports = {
  selector: '.scoped'
}
```

### Typescript support

Pollen exports its config as a `Config` type, which you can use to annotate your config file with JSDoc typings

```javascript
/** @type {import('pollen-css').Config} */
module.exports = {}
```

Alternatively use the included `defineConfig()` helper to get typescript support without JSDoc annotation

```javascript
const { defineConfig } = require('pollen-css/utils');

module.exports = defineConfig({ ... });
```
