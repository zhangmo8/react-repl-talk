# Thread Yielding
Yielding Strategies

Library provides three main yielding strategies:
- `interactive` - For urgent tasks (83ms chunks)
- `smooth` - For balanced, 60fps target tasks (13ms chunks)
- `idle` - For background tasks (5ms chunks)

&nbsp;

Which one do you pick?
> Scheduling the task keeps the page `interactive`/`smooth`/`idle`

<!--
three main strategies depending on the use case
- sets how long code can run before the next time it yields
- urgent: complete as fast as possible, allocates the most time
- smooth: balanced, focuses on achieving 60fps because 60fps over 1000s gives around 16ms per cycle, allotting 3ms per paint
- idle: background tasks, only 5ms
-->
