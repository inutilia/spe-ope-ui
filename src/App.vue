<template>
  <div id="app">
    <span>{{x1}}, {{y1}}</span>
    <svg id="myCanvas" width="300" height="300" @mousemove="showCoordinates">
      <line :x1=this.x1 :y1=this.y1 :x2=this.y1 :y2=this.x1 stroke="black"></line>
    </svg>
    <vs-button>Hello World</vs-button>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      canvas: null,
      x1: 0,
      y1: 0
    }
  },
  methods: {
    showCoordinates(e) {
      this.x1 = e.offsetX;
      this.y1 = e.offsetY;
    }
  },
}
</script>

<style scoped>
  #myCanvas {
    background-color: grey;
  }
</style>

