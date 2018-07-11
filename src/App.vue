<template>
  <div id="app">
    <todolist v-on:data="getData"></todolist>
    <deletes :taskList="data"></deletes>
    <hr>
    <child1></child1>
    <child2></child2>
  </div>
</template>

<script>
import todolist from './components/TodoList'
import deletes from './components/deletes'

import child1 from './components/child1'
import child2 from './components/child2'

export default {
  name: 'App',
  data () {
    return {
      data:""
    }
  },
  components: {
    todolist,
    deletes,
    child1,
    child2
  },
  methods: {
    getData(data){
      this.data=data
      console.log(data);
    }
  }
}
</script>

<style>

</style>
