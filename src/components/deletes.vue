<template>
    <ul>
        <li v-for="(item,index) in taskList">
                <div>             
                    <label>{{item.text}}</label>   
                    <button @click="del(index)">删除</button>         
                </div>
            </li>
        </ul>
</template>

<script>

export default {
    props:['taskList'],
    data () {
        return {

        }
    },
    created(){
        // alert(1);
        console.log(this.taskList)
    },
    methods: {
        del(index){
            this.taskList.splice(index,1) 
        }
    }
}
</script>

<style>

</style>
