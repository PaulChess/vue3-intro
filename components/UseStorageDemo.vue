<script setup lang="ts">
// import { stringify } from '@vueuse/docs-utils'
import { useStorage } from '@vueuse/core'
import { reactify } from '@vueuse/shared'
import YAML from 'js-yaml'

const stringify = reactify(
  (input: any) => YAML.dump(input, {
    skipInvalid: true,
    forceQuotes: true,
    condenseFlow: true,
    quotingType: '\'',
  }),
)

const state = useStorage('vue-use-local-storage', {
  name: 'Banana',
  color: 'Yellow',
  size: 'Medium',
  count: 0,
})
const text = stringify(state.value)
</script>

<template>
  <div>
    <input class="border border-sky-500 mr-2 pl-2 rounded-sm text-neutral-700" v-model="state.name" type="text">
    <input class="border border-sky-500 mr-2 pl-2 rounded-sm text-neutral-700" v-model="state.color" type="text">
    <input class="border border-sky-500 mr-2 pl-2 rounded-sm text-neutral-700" v-model="state.size" type="text">
    <input class="border border-sky-500 mr-2 -l-2 rounded-sm text-neutral-700" v-model.number="state.count" type="range" min="0" step="0.01" max="1000">

    <pre lang="json" class="mt-3 pl-1 text-sm">{{ text }}</pre>
  </div>
</template>

<style scoped>
.slidev-layout pre {
  font-family: 'Consolas,"Liberation Mono","Courier New",monospace' !important;
}
</style>