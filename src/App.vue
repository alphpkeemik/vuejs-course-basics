<template>
  <div id="app">
   <div>
     <input v-bind:value="message" />
   </div>
    <div>
      {{ message }}
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      message: 'I live on the component instance',
      foo: 5,
      bar: 3
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
