<script>
import todoForm from './components/todoForm.vue';
import todoList from './components/todoList.vue';
export default {
    data(){
        return{
            todo:[
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
        }
}
</script>

<template>
        <h1>Todo App</h1>
        <todo-form />
        <todo-list/>
</template>

