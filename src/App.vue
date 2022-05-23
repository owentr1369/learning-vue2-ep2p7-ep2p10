<template>
  <div id="app">
    <h1>HelloWorld</h1>
    <div id="obj">
      <h1>Bam nut de tang gia tri</h1>
      <h2>{{ dem }}</h2>
      <button v-on:click="handleIncrease">Increase</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      dem: 0,
    };
  },
  methods: {
    handleIncrease: function () {
      this.dem = this.dem + 1;
    },
  },
};
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
