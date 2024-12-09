# Thread Yielding
Quick Example
````md magic-move {lines: true}
```ts {all|3}
function someLongRunningTask() {
  for (let i = 0; i < 10000; i++) {
    doSomeWork()
  }
}

```
```ts {3-5}
function someLongRunningTask() {
  for (let i = 0; i < 10000; i++) {
    setTimeout(() => {
      doSomeWork()
    }, 0)
  }
}
```
```ts {all}
function someLongRunningTask() {
  for (let i = 0; i < 10000; i++) {
    setTimeout(() => {
      doSomeWork()
    }, 0)
  }
}
```
```ts {1}
import { yieldOrContinue } from 'main-thread-scheduling'

function someLongRunningTask() {
  for (let i = 0; i < 10000; i++) {
    setTimeout(() => {
      doSomeWork()
    }, 0)
  }
}
```
```ts {3,5-6}
import { yieldOrContinue } from 'main-thread-scheduling'

async function someLongRunningTask() {
  for (let i = 0; i < 10000; i++) {
    await yieldOrContinue('interactive')
    doSomeWork()
  }
}
```
````

<!--
we have some long running loop that does some work, 

[click] it will run this 10000 times before letting the browser work again

[click] we can yield with setTimeout. Immediate resolved promise is also similar. goes from 1 task with 10000 func calls to queueing 10000 smaller tasks

[click] can be hard to follow the flow with this pattern

[click] instead we can import

[click] and write it like this to achieve the same effect
-->
