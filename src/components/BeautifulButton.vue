<template>
  <button @click="$emit('click')">
    {{ value }}
  </button>
</template>

<script>
export default {
  name: 'BeautifulButton',
  props: ['value']
}
</script>

<style scoped>

</style>
