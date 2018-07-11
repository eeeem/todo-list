<template>
    <div>
        <h1>todo app</h1>
        <input type="text" v-model="content">
        <button @click="getText();testClick()">add</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            items:[{text:'A'},{text:'B'},{text:'C'}],
            content:""
        }
    },
    methods: {
        getText(){
            this.items.push({text:this.content});
            this.content="";
        },
        testClick(){
            this.$emit('data',this.items)
        },

    }
}
</script>

<style>

</style>
