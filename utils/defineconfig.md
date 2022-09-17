# defineConfig

Pollen exports a configuration helper function to give full typescript support in any file, including plain JS config files.

{% code title="pollen.config.js" %}
```javascript
const { defineConfig } = require('pollen-css/utils');

module.exports = defineConfig(pollen => ({ ... }));
```
{% endcode %}
