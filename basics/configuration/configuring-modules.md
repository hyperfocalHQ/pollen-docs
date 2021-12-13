# Configuring Modules

Every module in Pollen can be customised, overwritten, and extended. A _module_ is a collection of CSS variables with the same prefix, eg: `scale` (see [typography.md](../../modules/typography.md "mention")), `size` (see [layout.md](../../modules/layout.md "mention")), etc.

### Enabling and disabling&#x20;

Enable and disable whole module by passing `true` or `false` to the module in your config. All modules are enabled by default, set any you don't plan on using to `false` to further save on bundle size.

{% code title="pollen.config.js" %}
```javascript
module.exports = {
  modules: {
    scale: false,
    width: false,
    color: true
  }
}
```
{% endcode %}

### Overwriting

To overwrite a module, provide an object with all the values you want to use to the module in your config.

{% code title="pollen.config.js" %}
```javascript
module.exports = {
  modules: {
    scale: { /* custom type scale */ },
    letter: { /* custom letter spacing scale * }
  }
}
```
{% endcode %}

### Extending

Often you'll want to just add or tweak a few values from Pollen's defaults instead of disabling or overwriting outright.&#x20;

To do this Pollen provides all of its defaults as an argument to a configuration _function_ rather than a plain object. Spread the appropriate key into a new object on the module to extend or overwrite Pollen's defaults.

{% code title="pollen.config.js" %}
```javascript
module.exports = (pollen) => ({
  modules: {
    scale: { ...pollen.scale, '000': '0.6875rem' },
    letter: {...pollen.letter, xxl: '0.1em' }
   } 
});
```
{% endcode %}

These defaults are also provided in the `defineConfig` typescript helper

```javascript
const { defineConfig } = require('pollen-css/utils');

module.exports = defineConfig(pollen => ({
  modules: {
    scale: { ...pollen.scale, '000': '0.6875rem' },
    letter: {...pollen.letter, xxl: '0.1em' }
   } 
  })
);
```
