---
layout: image-right
image: https://images.unsplash.com/photo-1662685315883-71b852331b5e?q=80&w=3270&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

# Thread Yielding

Let the browser do its thing

- Blocking tasks causes the UI to lock up
- JS Event Loop
  - Single threaded
  - `requestIdleCallback`, `requestAnimationFrame`, `setTimeout`

TL;DR: Pause your own code to let the browser catch up

<!--
- as we know blocking tasks cause the UI to freeze
- this is due to how JS in the browser runs on a single thread
- some knowledge of how event loop works can be helpful to understand this issue
- traditionally relied on things like  rAF or sTO with 0ms to defer tasks
- yields to browser so it can clean up task/microtasks, perform render and paint cycles, etc.
-->
