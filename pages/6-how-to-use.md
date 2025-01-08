---
class: text-lg
---

# How to use

```shell
[npm|yarn|pnpm] i @zhangmo8/repl-react 
```

```ts
import { Repl } from '@zhangmo8/repl-react'

const Demo = () => {
  const defaultCode = `xxxx`
  return <Repl defaultCode={defaultCode} />
}
```

tips: 确保你的 vite 版本在 6 以上。如果不是，在本地环境中可能会有 wasm 错误。然而，这并不影响打包后的效果。有关详细信息，你可以看[这里](https://github.com/vitejs/vite/issues/8427)。

如：vite < 6.0，则需要额外增加一下配置

```ts
// vite.config.ts
import { defineConfig } from 'vite'
export default defineConfig({
  optimizeDeps: {
    exclude: ['@zhangmo8/repl-react'],
  },
})
```
