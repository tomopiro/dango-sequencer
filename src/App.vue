<template>
  <div id="app">
    <Dango ref="dango" id="dango"/>
    <PlayButton @click="moveDango"/>
  </div>
</template>

<script>
import Dango from './components/dango-img.vue'
import PlayButton from './components/play-button.vue'
import gsap from "gsap";

export default {
  name: 'App',
  components: {
    Dango,
    PlayButton
},
  methods: {
    moveDango () {
      var tl = gsap.timeline({repeat: -1, repeatDelay: 0, onComplete: null});
      tl.to("#dango", {x: 10, duration: 2})
      tl.to("#dango", {x: 500, duration: 2})
    }
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
