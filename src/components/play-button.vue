<template>
  <img v-on:click="play" src="@/assets/Play.svg" alt="" class="play-button">
</template>

<script>
export default {
  data () {
    return {
      x: 200
    }
  },
  methods: {
    play: function() {
      
    }
  }
}
</script>

<style scoped>
.play-button {
  
  width: 128px;
  height: 128px;
}
</style>