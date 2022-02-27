<script>

import todosData from './data'

export default {
    name:'todoApp',
    data(){
        return{
            todos:todosData,
            message:''
        }
    },
    methods:{
        logPost:function(){
            console.log(this.message)
            console.log(this.todos)
        }
    }
}
</script>


<template>
    <div class='app'>
        <h1>todo-App</h1>
        <div class="post">
            <form class='post' @submit.prevent='logPost'>
                <input type="text" v-model='message'> <button type='submit'>submit</button>
            </form>
        </div>
    </div>
</template>


<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
html{
    background-color: #1a1a1a;
    color: white;
    font-family: 'poppins',sans-serif;
}
.app{
    display: flex;
    align-self: center;
    align-items: center;
    flex-direction: column;
}

ul{
    padding: 0;
    list-style: none;
}
li{
    width: 100%;
}
label{
    display: inline-block;
    width: 200px;
}
.check{
    float: right;
}
</style>
