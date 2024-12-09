---
class: text-xl
---

# React Transitions
What are they?

Marks a state update as a <span class="underline underline-2 italic">Transition</span>

- State updates are actually synchronous
- Transitions will defer/de-prioritize the update
- Allows more important updates and user input events to take priority

<!--
syncrhonous
- when we write state updates, they don't feel synchronous
- setState schedules the state update and batches multiple together, not firing right away
- when dispatched, it does happen synchronously and can block the UI

defer
- tells React that state update isn't urgent and can be done later
- lets more important things such as non-transitions and inputs to take place
-->
