<script>
import todoForm from './components/todoForm.vue';
import todoList from './components/todoList.vue';
export default {
    data(){
        return{
            todos1:[
                {
                    id:1,
                    todo:'make pancakes'
                },
                {
                    id:2,
                    todo:'ride bicycle'
                },
                {
                    id:3,
                    todo:'code'
                },
                {
                    id:4,
                    todo:'watch tv'
                }
            ]
        }},
        components:{
            todoForm,
            todoList
        },
}
</script>

<template>
        <h1>Todo App</h1>
        <todo-form />
        <todo-list :todos=todos1 />
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
</style>
