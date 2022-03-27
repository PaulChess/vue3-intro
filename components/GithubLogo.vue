<script setup lang="ts">

const props = defineProps({
  url: {
    type: String,
    default: ''
  }
})

function jumpGithub() {
  window.open(props.url, '_blank')
}

</script>

<template>
  <carbon-logo-github  @click="jumpGithub" class="cursor-pointer" />
</template>