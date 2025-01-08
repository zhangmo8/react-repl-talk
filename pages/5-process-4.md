---
class: text-lg
---

# Babel Replace To SWC

````md magic-move {lines: true}

```ts
// preview component
import { transform } from "@babel/core";

const result = babel.transform("code();", babelOptions, function(err, result) {
  return result;
});

// render
iframe.contentWindow.body.contentDocument.write(result.code);
iframe.contentWindow.body.contentDocument.close();
```

```ts
// preview component
import { transform } from "@swc/core";

const result = await swc.transform("code();", swcOptions);

// render
iframe.contentWindow.body.contentDocument.write(result.code);
iframe.contentWindow.body.contentDocument.close();
```
````
