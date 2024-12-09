---
class: text-lg
---

# Interaction to Next Paint (INP)
Sluggish UIs

<span class="inline-block mt-5">❌</span> What causes poor INP?

### Blocking tasks during time of input
  - Ads refreshing
  - Tracking events

### Handlers taking long to resolve
  - Long, synchronous blocking tasks
  - Performing tasks not visible to the user
### Expensive style calculations
  - State changes causing expensive UI rendering

<!--
each of the 3 parts can cause INP to go up

- input delay
  - slow event handler not finished yet (double/rage clicks)
  - background tasks like ads/tagging/3rd party
- processing time
  - long blocking task (complex loop, awaiting long response)
- presentation delay
  - forced reflow
  - expensive rendering
-->
