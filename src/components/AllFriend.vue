<template>
    <div id="allfriend">
       <h2> All Friend </h2>
       <div v-for="(friend, index) in friends" :key="index">
            <h5>{{ friend.name }}</h5>
       </div>
    </div>
</template>


<script>
export default {
    name: 'AllFriend',
    props:['friends'],
    data() {
        return {
          
        }
    },
}
</script>


<style scoped>
    nav{
        text-align: center;
    }
    nav ul{
        padding: 0;
    }
    nav li{
        display: inline-block;
        list-style-type: none;
        margin: 0px;
        padding: 8px;
    }
</style>