<template>
    <div>
        <nav>
            <ul>
                <li><a herf="">Home</a></li>
                <li><a herf="">Post</a></li>
                <li><a herf="">About</a></li>
                <li><a herf="">Contact</a></li>
            </ul>
        </nav>
    </div>
</template>


<script>
export default {
    name: 'NavBar',
    data() {
        return {
            
        }
    },
}
</script>


<style>
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