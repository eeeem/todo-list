<template>
    <ul>
        <li v-for="(item,index) in items">
                <div>             
                    <label>{{item.text}}</label>   
                    <button @click="del(index)">删除</button>         
                </div>
            </li>
        </ul>
</template>

<script>

export default {
    computed:{
        items(){
            return this.$store.state.items      
        }
    },
    methods: {
        del(index){
            this.items.splice(index,1) 
        } 
    }
}
</script>

<style>

</style>
