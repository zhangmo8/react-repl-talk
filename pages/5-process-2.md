---
class: text-lg
---

# Different

<div class="flex flex-col justify-center h-full">

<div class="flex-1">

````md magic-move {lines: true}

```html {all|2-8|all}
<script type="text/babel">
  function App() {
    const [name, setName] = React.useState("codelab")
    return <div>hello, {name}</div>
  }
  const container = document.getElementById('root')
  const root = ReactDOM.createRoot(container)
  root.render(<App/>)
</script>
```

```html {all|1,2|all}
<script type="text/babel" data-plugins="transform-es2015-modules-umd">
  import React from "react"

  function App() {
    const [name, setName] = React.useState("codelab")
    return <div>hello, {name}</div>
  }
  const container = document.getElementById('root')
  const root = ReactDOM.createRoot(container)
  root.render(<App/>)
</script>
```

````

</div>

<div class="flex-1">

```ts
import React from "react"
import { createRoot } from "react-dom/client";

export default function App() {
  const [name, setName] = React.useState("codelab")
  return <div>hello, {name}</div>
}

createRoot(document.getElementById('root')).render(React.createElement(App));
```

</div>

</div>
