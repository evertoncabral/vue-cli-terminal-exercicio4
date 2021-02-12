<template>
  <div id="app">
    <button @click="counter.a++">Click para contar o elemento 'a'</button>
    {{ counter }}
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      counter: {
        x: 0,
      },
    }
  },
  mounted() {
    this.$set(this.counter, "y", 1);
    this.counter = {...this.counter,...{ a: 2, b: 3} };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
