<template>
  <div class="input-form" @submit.prevent>
    <form @submit.>
      <input
          v-model="task.text"
          type="text"
          class="form-input"
          placeholder="Input todo here..."
      />
      <button class="button-add" @click="addTodo">Add Todo</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      task: {
        text: '',
      }
    }
  },
  methods: {
    addTodo() {
      if (this.task.text.length === 0) {
        return;
      }
      this.task.id = Date.now();
      this.$emit('create', this.task);
      this.task.text = '';
    }
  }
}
</script>

<style scoped>
.input-form {
  padding: 15px;
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