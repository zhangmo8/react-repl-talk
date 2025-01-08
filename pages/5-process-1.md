---
class: text-lg
---

# Start with the HTML

HTML File

````md magic-move {lines: true}
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Document</title>
</head>
<body>
</body>
</html>
```

```html {*|5,6,9-17|*}
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Document</title>
  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
</head>
<body>
  <script>
    function App() {
      const [name, setName] = React.useState("codelab")
      return <div>hello, {name}</div>
    }
    const container = document.getElementById('root')
    const root = ReactDOM.createRoot(container)
    root.render(<App/>)
  </script>
</body>
</html>
```

```html {*|7,10|*}
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Document</title>
  <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
  <script src="https://cdn.bootcdn.net/ajax/libs/babel-standalone/7.20.6/babel.min.js"></script>
</head>
<body>
  <script type="text/babel">
    function App() {
      const [name, setName] = React.useState("codelab")
      return <div>hello, {name}</div>
    }
    const container = document.getElementById('root')
    const root = ReactDOM.createRoot(container)
    root.render(<App/>)
  </script>
</body>
</html>
```
````
