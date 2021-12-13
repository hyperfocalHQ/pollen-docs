# Extending Pollen

Just as you can customise, extend, and overwrite the included modules in Pollen, you can also use Pollen to generate your own completely custom design system.&#x20;

### Custom modules

Every key in Pollen's `modules` configuration is turned into a family of CSS variables. The module name becomes the variable prefix, and a property is generated for each key in the module object.

For example this configuration would generate a new group of variables as `--typeset-*`

{% tabs %}
{% tab title="Configuration" %}
```javascript
module.exports = {
  modules: {
    typeset: {
      '0': 'var(--scale-0)/1.3 var(--font-sans)',
      '1': 'var(--scale-1)/1.5 var(--font-sans)',
      '2': 'var(--scale-2)/1.4 var(--font-sans)',
      '3': 'var(--scale-3)/1.2 var(--font-sans)',
      '4': 'var(--scale-4)/1.1 var(--font-sans)',
    }
  }
}
```
{% endtab %}

{% tab title="Generated CSS" %}
```css
:root {
  // The rest of Pollen's CSS
  --typeset-0: var(--scale-0)/1.3 var(--font-sans);
  --typeset-1: var(--scale-1)/1.5 var(--font-sans);
  --typeset-2: var(--scale-2)/1.4 var(--font-sans);
  --typeset-3: var(--scale-4)/1.1 var(--font-sans);
}
```
{% endtab %}
{% endtabs %}

Property keys in module configuration are automatically kebab-cased. For example `pageWidth` in the [`grid` module](../../modules/grid.md) becomes `--grid-page-width`.

### Configuration logic

Since Pollen's configuration is just JavaScript, you can run any logic you need to generate your design system configuration as long as it's synchronous.&#x20;

The above example could be simplified with a `makeTypeset()` function like so

```javascript
function makeTypeset(scale, lh) {
  return `var(--scale-${scale})/${lh} var(--font-sans)`;
}

module.exports = {
  modules: {
    typeset: {
      '0': makeTypeset(0, 1.3),
      '1': makeTypeset(1, 1.5),
      '2': makeTypeset(2, 1.4),
      '3': makeTypeset(3, 1.2),
      '4': makeTypeset(4, 1.1)
    }
  }
}
```

This can be especially powerful for things like generating opacities from HEX colours, value scales based on ratios, and more.
