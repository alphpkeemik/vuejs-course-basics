<template>
  <button @click="$emit('click')">
    {{ value }}
  </button>
</template>

<script>
export default {
  name: 'BeautifulButton',
  props: {
    value: {
      type: String
    }
  }
}
</script>

<style scoped>

</style>
