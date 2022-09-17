# fluid

Generates complex CSS `clamp()` functions for robust fluid units, used for Pollen's inbuilt fluid typography scale

```typescript
fluid(
  minSize: number, 
  maxSize: number, 
  minWidth?: number, 
  maxWidth?: number
)
```

{% code title="pollen.config.js" %}
```javascript
const { fluid } = require('pollen-css/utils');

module.exports = (pollen) => ({
  modules: {
    fluidFontSize: {
      '0': fluid(14, 16)
    }
  }    
});
```
{% endcode %}

| Property   | Default | Required | Description                        |
| ---------- | ------- | -------- | ---------------------------------- |
| `minSize`  |         | Yes      | Smallest value of the size (in px) |
| `maxSize`  |         | Yes      | Largest value of the size (in px)  |
| `minWidth` | `480`   | No       | Screen width fluid range begins    |
| `maxWidth` | `1280`  | No       | Screen width fluid range ends      |
