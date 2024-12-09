---
class: text-lg
---

# React Transitions
Practical Example
````md magic-move {lines: true}
```tsx {all|16-19|5-14|7,12}
function Combobox() {
  const [searchInput, setSearchInput] = useState('');
  const [items, setItems] = useState([]);

  function handleChange(e) {
    const inputValue = e.target.value;
    setSearchInput(inputValue);
    
    if (inputValue.length === 0) return;

    const newItems = getNewItems(inputValue)
    setItems(newItems);
  }

  return (
    <>
      <input type="text" value={searchInput} onChange={handleChange} />
      {items.map()}
    </>
  );
}
```

```tsx {7,13-15}
function Combobox() {
  const [searchInput, setSearchInput] = useState('');
  const [items, setItems] = useState([]);

  function handleChange(e) {
    const inputValue = e.target.value;
    setSearchInput(inputValue);
    
    if (inputValue.length === 0) return;

    const newItems = getNewItems(inputValue)
    
    startTransition(() => {
      setItems(newItems);
    });
  }

  return (
    <>
      <input type="text" value={searchInput} onChange={handleChange} />
      {items.map()}
    </>
  );
}
```
````

<!--
super simple combobox-like component

[click] simple text input with list of rendered items

[click] 
we have change handler that updates the input value and sets the new list of items

[click] these two state updates are actually batched together into one, meaning that the search input won't get updated until the new items have finished in the same re-render

[click] we can alleviate this by wrapping in transition 

tells react that this update isn't urgent and can wait, let other updates happen first

Immediate UI Feedback: Users see their input reflected instantly
-->
