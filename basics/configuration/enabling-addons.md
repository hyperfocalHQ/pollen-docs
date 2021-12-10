# Enabling Addons

Pollen comes with several optional [Broken link](broken-reference "mention"). Enable them by setting the appropriate module to `true` in your Pollen config.

{% code title="pollen.config.js" %}
```javascript
module.exports = {
  modules: {
    grid: true,
    color: true
  }
}
```
{% endcode %}

Likewise set any default module to `false` to disable it completely&#x20;

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
