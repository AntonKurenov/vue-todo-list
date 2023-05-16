<template>
  <div>
    Hello world!!
  </div>
  <div>
    <button @click="addPlus"> +</button>
    <button @click="addMinus"> -</button>
  </div>
  <div>Plus {{ pluses }}</div>
  <div>Minus{{ minuses }}</div>
</template>

<script>
export default {
  data() {
    return {
      pluses: 0,
      minuses: 0,
    }
  },
  methods: {
    addPlus() {
      this.pluses += 1;
    },
    addMinus() {
      this.minuses += 1;
    }
  }
}

</script>

<style>

</style>