<template>
  <div id="app" v-on:mousemove="handlePosition">
    <h1>HelloWorld</h1>
    <div id="obj">
      <h1>Bam nut de tang gia tri</h1>
      <h2>{{ dem }}</h2>
      <button v-on:click="handleIncrease">Increase</button>
      <p>Toa do cua chuot: {{ x }} : {{ y }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      dem: 0,
      x: 0,
      y: 0,
    };
  },
  methods: {
    handleIncrease: function () {
      this.dem = this.dem + 1;
    },
    handlePosition: function (event) {
      this.x = event.clientX;
      this.y = event.clientY;
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
