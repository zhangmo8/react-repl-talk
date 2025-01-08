---
class: text-lg
---

# Replace To ESM

````md magic-move {lines: true}

```html
<script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
<script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
<script src="https://cdn.bootcdn.net/ajax/libs/babel-standalone/7.20.6/babel.min.js"></script>
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

```html
<script type="importmap">
{
  "imports": {
    "react": "https://esm.sh/react@18.2.0?dev",
    "react-dom": "https://esm.sh/react-dom@18.2.0?dev",
    "react-dom/client": "https://esm.sh/react-dom@18.2.0/client?dev"
  },
  "scopes": {}
}
</script>
<script type="module">
  import { useState } from 'codelab';

  function App() {
    const [name, setName] = useState("codelab")
    return <div>hello, {name}</div>
  }
  const container = document.getElementById('root')
  const root = ReactDOM.createRoot(container)
  root.render(<App/>)
</script>
```

````
