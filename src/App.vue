<template>
  <div id="app" v-on:mouseover="handlePosition">
    <h1>HelloWorld</h1>
    <div id="obj">
      <h1>Bam nut de tang gia tri</h1>
      <h2>{{ dem }}</h2>
      <button v-on:click="handleIncrease">Increase</button>
      <p>Toa do cua chuot: {{ x }} : {{ y }}</p>
      <span v-on:mouseover="handleMouseOver">Dung su kien</span>
      <!-- <span v-on:mouseover.stop="">Dung su kien</span> -->
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
    handleMouseOver: function (event) {
      event.stopPropagation();
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
