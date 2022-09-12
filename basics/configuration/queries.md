# Media & Supports

CSS variables can be globally responsive. By updating variables in `@media` or `@supports` queries, you can adapt your entire interface instantly.

Pollen supports both of these queries through the `media` and `supports` options in `pollen.config.js`. By updating [modules](broken-reference) here they will be changed if the query given is matched.

{% tabs %}
{% tab title="Configuration" %}
```javascript
module.exports = {
  media: {
    '(min-width: 640px)': {
      scale: {
        0: '1.125rem'
      }      
    }
  },
  supports: {
    '(display: grid)': {
      grid: {
        content: 'var(--grid-12)'
      }
    } 
  }
}
```
{% endtab %}

{% tab title="Generated CSS" %}
```css
:root {
  ...Pollen modules
}

@media (min-width: 640px) {
  :root {
    --scale-0: 1.125rem;
  }
}

@supports (display: grid) {
  :root {
    --grid-content: var(--grid-12)
  } 
}
```
{% endtab %}
{% endtabs %}
