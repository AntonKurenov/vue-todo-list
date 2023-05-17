<template>
  <div class="todo-item">
    <div>{{ todo.text }}</div>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true,
    }
  }

}
</script>

<style scoped>

.task-item {

}

</style>