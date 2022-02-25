<script>
import todoForm from './components/todoForm.vue'
export default {
    data(){
        return{
            Pmessage:'',
            checkedId:[],
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
        },
        methods:{
            pushy:function(){
                const todos1 = this.todos1
                console.log(this.Pmessage)
                const newId = todos1.length + 1
                console.log(newId)
                todos1.push({id:newId,todo:this.Pmessage})
            },
            logged(){
                for(let i = 0; i < this.checkedId.length;i++){
                    const todoId = this.checkedId[i] - 1;
                    this.todos1.splice(todoId,1)
                }
                }
            },
        
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

    <div class="list">
        <form @submit.prevent="logged">
            <ul>
                <li v-for="item in todos1" :key='item.id'>
                    <h3>
                        <label for="item.id">{{item.todo}}</label>
                        <input type="checkbox" name='item.todo'
                            :value='item.id' v-model="checkedId" >
                    </h3>
                </li>
            </ul>
            <button type='submit' class='check'>check tasks</button>
        </form>
    </div>
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
