<template>
  <div id="app">
    <Generator msg="Welcome"/>
  </div>
</template>

<script>
import Generator from './components/Generator.vue'

export default {
  name: 'App',
  components: {
    Generator
  }
}
</script>

<style lang="sass">
  html
    background: rgb(random(255), random(255), random(255))
    
    #app
      font-family: Avenir, Helvetica, Arial, sans-serif
      -webkit-font-smoothing: antialiased
      -moz-osx-font-smoothing: grayscale
      text-align: center
      color: #2c3e50
      margin-top: 60px
</style>
