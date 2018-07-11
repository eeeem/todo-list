<template>
    <div>
        <h1>todo app</h1>
        <input type="text" v-model="content">
        <button @click="getText()">add</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            content:""
        }
    },
    computed:{
        items(){
            return this.$store.state.items
        }
    },
    methods: {
        getText(){
            this.items.push({text:this.content});
            this.content="";
        }
    }
}
</script>

<style>

</style>
