<template>
  <div class="app">
    <header>Todo List</header>
    <add-form @create="createTodo"/>
    <TodoList :tasks="tasks"/>
  </div>
</template>

<script>
import AddForm from "./components/AddForm.vue";
import TodoList from "./components/TodoList.vue";

export default {
  components: {TodoList, AddForm},
  data() {
    return {
      tasks: [
        {id: 1, text: 'Hello world!'},
        {id: 2, text: 'Learn Vue!'},
      ],
    }
  },
  methods: {
    createTodo(todo) {
      // todo.id = this.tasks.length;
      this.tasks.push(todo);
    },
  }
}

</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 10px;
}


form {
  padding: 10px;
}




</style>