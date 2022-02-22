<script>
import todoForm from './components/todoForm.vue'
import todoList from './components/todoList.vue';
export default {
    data(){
        return{
            Pmessage:'',
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
        methods:{
            pushy:function(){
                const todos1 = this.todos1
                console.log(this.Pmessage)
                const newId = todos1.length + 1
                console.log(newId)
                todos1.push({id:newId,todo:this.Pmessage})
            }
        }
}
</script>

<template>
    <h1>Todo App</h1>
    <!--div class='post'>
        <form class="form" @submit.prevent='pushy'>
            <input type="text" v-model='message'> <button 
           type='submit'>submit</button>
        </form>
    </div -->
    <todo-form v-model:message=Pmessage @submit="pushy" />
        <todo-list :todos=todos1 />
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
html{
    background-color: #1a1a1a;
    color: white;
    font-family: 'poppins',sans-serif;
}
#app{
    display: flex;
    align-self: center;
    align-items: center;
    flex-direction: column;
}
</style>
