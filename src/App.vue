<template>
  <div class="answers">
    <Answers/>
  </div>
</template>

<script>
import Answers from './components/Answers.vue'
export default {
  name: 'App',
  components: {
    Answers
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}

</style>
