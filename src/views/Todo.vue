<template>
  <div>
    <h1>Todo List</h1>
    <input v-model="newtask">
    <button @click="addTask">Add</button>
    <ul>
      <li v-for="todo in todos" :key="todo">{{todo}}</li>
    </ul>
  </div>
</template>


<script>
export default {
  data: function() {
    return {
      newtask : '',
      todos: ["first task", "Second task"]
    };
  },
  methods : {
      addTask() {
         this.todos.push(this.newtask),
         this.newtask = '' 
      }
  }
};
</script>
