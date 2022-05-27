<template>
  <div id="app">
    <div class="stage" @click="moveDango">
      <div class="note">クリックしたあたりまでスライドします</div>
      <Dango ref="dango" />
    </div>
  </div>
</template>

<script>
import Dango from './components/dango-img.vue'

export default {
  name: 'App',
  components: {
    Dango
  },
  methods: {
    moveDango (ev) {
      // クリックされたX座標までスライドする
      this.$refs.dango.moveTo(ev.offsetX)
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
