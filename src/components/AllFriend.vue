<template>
    <div id="allfriend">
       <h2> All Posts </h2>
       <input type="text" v-model="searchTerm" placeholder="Search">
       <hr>
       <div v-for="post in filtersearch" :key="post.id">
            <h3>{{ post.id }}</h3>
            <h3>{{ post.title }}</h3>
            <hp>{{ post.body | snippet }}</hp>
            <hr>
       </div>
    </div>
</template>


<script>
import axios from 'axios'
export default {
    name: 'AllFriend',
    props:['friends'],
    data() {
        return {
            posts:[],
            searchTerm: ''
        }
    },

    computed:{
        filtersearch(){
           return this.posts.filter(post =>{
                return post.title.match(this.searchTerm)
            });
        }
    },

    methods: {
       
    },

    created() {
        axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response =>{
            this.posts = response.data
            // console.log(response)
        })
        .catch(error =>{
            console.log(error)
        });
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