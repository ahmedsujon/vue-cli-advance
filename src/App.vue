<template>
  <div id="app">
    <h2>{{title}}</h2>
    <NavBar></NavBar>
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'

export default {
  name: 'App',

  data() {
    return {
      title: 'Hello World!'
    }
  },
  components:{
    NavBar
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
