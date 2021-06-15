<template>
  <div id="app">
    <h2>{{title}}</h2>
    <NavBar></NavBar>
    <AllFriend></AllFriend>
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'
import AllFriend from './components/AllFriend'

export default {
  name: 'App',

  data() {
    return {
      title: 'Hello World!',

    }
  },
  components:{
    NavBar,
    AllFriend,
  },

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
