<template>
    <div class="tasks" v-for="task in tasks">
    </div>
</template>

<script>
export default {
  props: {
    tasks: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style scoped>
.tasks {
  margin: 10px;
  padding: 10px;
  border: aqua 2px solid;
}
</style>