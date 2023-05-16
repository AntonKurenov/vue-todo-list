<template>
  <div class="app">
    <header>Todo List</header>
    <div class="input-form" @submit.prevent>
      <form @submit.>
        <input
            v-bind:value="text"
            @input="text = $event.target.value"
            type="text"
            class="form-input"
            placeholder="Input todo here..."
        />
        <button class="button-add" @click="addTodo">Add Todo</button>
      </form>
    </div>
    <div class="tasks" v-for="task in tasks">
      <div>{{ task.text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        {id: 1, text: 'Hello world!'},
        {id: 2, text: 'Learn Vue!'},
      ],
      text: '',
    }
  },
  methods: {
    addTodo() {

      const newTodo = {
        id: this.tasks.length,
        text: this.text,
      }
      this.tasks.push(newTodo);
      this.text = '';
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

.input-form {
  padding: 15px;
}

form {
  padding: 10px;
}

.tasks {
  margin: 10px;
  padding: 10px;
  border: aqua 2px solid;
}

.form-input {
  height: 100%;
  border: aqua 2px solid;
}

.button-add {
  height: 100%;
  margin-left: 20px;
}
</style>