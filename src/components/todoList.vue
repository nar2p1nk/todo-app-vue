
<script>
export default {
    props:{todos:Array}
}
</script>

<template>
    <div class="list">
        <h2></h2>
        <form >
            <ul>
                <li v-for="item in todos" :key='item.id'>
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
