<template>
  <div id="app">
   <div>
     <input
       :value="message"
       @input="onInput"
     />
     <button @click="onSubmit">
        Submit
     </button>
     <div>
       <label>
         <input
           :checked="submitAnonymously"
           @change="toggleSubmitAnonymously"
           type="checkbox"
         />
         Submit anonymously
       </label>
     </div>
   </div>
    <div>
      {{ message }}
      <template v-if="submitAnonymously">
        <div  class="submitAnonymouslyTrue">
          You are going to submit anonymously, just reminding you.
        </div>
        <div class="submitAnonymouslyFalse">
          You are going to submit by your name.
        </div>
      </template>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      message: 'I live on the component instance',
      submitAnonymously: false
    }
  },
  methods: {
    onInput (event) {
      this.message = event.target.value
    },
    toggleSubmitAnonymously (event) {
      this.submitAnonymously = !this.submitAnonymously
    },
    onSubmit () {
      console.log(this.message)
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
