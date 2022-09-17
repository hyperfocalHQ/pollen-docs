# shimmie

CSS variables aren't supported on IE11, so Pollen ships with a dynamic polyfill called `shimmie`. Shimmie will check for support and, if required, dynamically load and apply the excellent [`css-vars-ponyfill`](https://jhildenbiddle.github.io/css-vars-ponyfill/#/) shim with sane configuration.

{% code title="app.js" %}
```javascript
import { shimmie } from 'pollen-css/utils';

shimmie();
```
{% endcode %}
