<script setup lang="ts">

function jumpToVueUse() {
  window.open('https://vueuse.org/functions.html', '_blank')
}

</script>

<template>
  <img class="w-50" src="https://d33wubrfki0l68.cloudfront.net/a5780e53fee68ddd1cd73a00484151d2d052cb4d/b7469/logo-vertical.png" @click="jumpToVueUse" />
</template>

<style scoped>
img {
  cursor: pointer;
}
</style>
