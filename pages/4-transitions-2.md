---
class: text-xl
---

# React Transitions
Simple Example

````md magic-move {lines: true}
```tsx {all|6-8,12}
import { useState } from 'react'

function Counter() {
  const [count, setCount] = useState(0)
  
  function handleClick() {
    setCount(count + 1)
  }

  return (
    <div>
      <button onClick={handleClick}>Increment</button>
      <div>Count: {count}</div>
    </div>
  )
}
```

```tsx {1,6-10}
import { useState, startTransition } from 'react'

function Counter() {
  const [count, setCount] = useState(0)
  
  function handleClick() {
    startTransition(() => {
        setCount(count + 1)
    })
  }

  return (
    <div>
      <button onClick={handleClick}>Increment</button>
      <div>Count: {count}</div>
    </div>
  )
}
```
````

<!--
very simple component

[click] we have a button with handler that changes state

[click] we can wrap the state change in transition 

easy, but not too useful, look at better example
-->
