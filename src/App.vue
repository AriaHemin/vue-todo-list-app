<template>
  <TodoList />
</template>

<script>
import TodoList from './components/todoList.vue';

export default {
  name: 'App',
  components: {
    TodoList
},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
