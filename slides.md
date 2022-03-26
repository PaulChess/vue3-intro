---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: 	https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# font family
fonts:
  # 用于代码块、内联代码等
  mono: 'DM mono'
  # 基础字体
  sans: 'Robot'
  # 与 windicss 的 `font-serif` css 类一同使用
  serif: 'Robot Slab'
---

# Vue3 Introduction <logos-vue />

同花顺 T2 职级课 -- Vue3 专题

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: center
---

# Composition API  <logos-vue />

---

##### Vue2 Components

<div grid="~ cols-2" class="gap-10">

```javascript
<template>
  <!-- -->
</template>

<script>
import Vue from 'vue'
import Foo from './components/Foo.vue'
import { mixinBar } from './mixins/bar'

export default Vue.extend({
  components: {
    Foo,
  },
  mixins: {
    mixinBar,
  },
  data() {
    return {};
  },
  methods: {},
  created() {}
})
</script>
```

<div>

###### The Problem

<div class="mt-2">

<v-clicks>

- "Scaffolding code" for each component
- Extensibility
- TypeScript support

</v-clicks>

</div>

</div>

</div>

---

### Vue3 learning resource recommend

<div class="mt-4 gap-12" grid="~ cols-2">

<div class="mt-2">

- 书籍:《Vue.js 设计与实现》
- 在线课程: 《极客时间-玩转 Vue3 全家桶》
- 新文档: https://staging-cn.vuejs.org/
- Awesome Vue: https://github.com/vuejs/awesome-vue
- Vue3 源码: https://github.com/vuejs/core
- 优质博客: https://antfu.me/posts
- 优质 Vue3 组件库: [移动端 Vant](https://github.com/youzan/vant)、[PC端 NaiveUI](https://github.com/TuSimple/naive-ui)
- 优质起手模板: https://github.com/antfu/vitesse
- Vue3 生态链: Pinia、Vitest、VueRouter4...
</div>

<img src="https://pic1.zhimg.com/v2-77cb108aa2af3626c2332253d9b54856_720w.jpeg?source=d16d100b" />

</div>
