---
class: full
---

# Detail

Analysis

<v-clicks>

- **layouts**
- **environmental isolation**
- **iframe load static**
- **linkage**

</v-clicks>

<div class="flex justify-center" v-show="$slidev.nav.clicks === 1">
  <img src="../images/playground.png" />
</div>

<div class="flex justify-center h-full" v-show="$slidev.nav.clicks === 2">
  <img src="../images/iframe.png" />
</div>


<div class="flex justify-center w-full" v-show="$slidev.nav.clicks === 3">
  <img src="../images/importMap.png" />
</div>

<!--
- 分析布局和 Dom 元素
- 隔离项目内的 react 实例 和 renderer 中的 React 实例
  - 环境隔离方案 -> iframe
- 分析渲染过程
-->
