<template>
  <div id="app" v-on:mouseover="handlePosition">
    <h1>HelloWorld</h1>
    <div id="obj">
      <h1>Bam nut de tang gia tri</h1>
      <h2>{{ dem }}</h2>
      <button v-on:click="handleIncrease">Increase1</button>
      <button v-on:click="dem++">Increase2</button>
      <p>Toa do cua chuot: {{ x }} : {{ y }}</p>
      <p>Gia tri: {{ dem > 20 ? "qua 20 r" : "chua qua 20" }}</p>
      <span v-on:mouseover="handleMouseOver">Dung su kien</span>
      <!-- <span v-on:mouseover.stop="">Dung su kien</span> -->
    </div>
    <div class="hello">
      <input type="text" v-on:keyup.space.enter="handleKeyboard" />
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
    handleKeyboard: function () {
      alert("Helloworld");
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
