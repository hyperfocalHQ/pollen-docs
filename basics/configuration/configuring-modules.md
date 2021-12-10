# Configuring Modules

Every module in Pollen can be customised, overwritten, and extended. A _module_ is a collection of CSS variables with the same prefix, eg: `scale` (see [typography.md](../../modules/typography.md "mention")), `size` (see [layout.md](../../modules/layout.md "mention")), etc.

To configure a module, provide an object to the appropriate key under `modules` in your config

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

### Extending defaults

Providing an object to a module like above will overwrite that module. Often you'll want to just tweak a few values from Pollen's defaults instead, or add more values to an existing module.&#x20;

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
