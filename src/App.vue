<template>
  <div id="app">
    <h2>{{title}}</h2>
    <NavBar></NavBar>
    <AllFriend :friends="friends"></AllFriend>
    <OnlineFriend :friends="friends"></OnlineFriend>
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'
import AllFriend from './components/AllFriend'
import OnlineFriend from './components/OnineFriend'

export default {
  name: 'App',

  data() {
    return {
      title: 'Hello World!',

        friends:[
                {name: 'A', online: true},
                {name: 'B', online: true},
                {name: 'C', online: false},
                {name: 'D', online: true},
                {name: 'E', online: false},
                {name: 'F', online: false},
            ]
    }
  },
  components:{
    NavBar,
    AllFriend,
    OnlineFriend
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
