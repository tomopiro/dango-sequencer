<template>
  <div class="box-dango"
    :style="{
      transform: `translate(${x}px, 250px)`
    }"
  />
</template>

<script>
export default {
  data () {
    return {
      x: 500
    }
  },
  methods: {
  }
}
</script>

<style scoped>
.box-dango {
  position: absolute;
  width: 128px;
  height: 128px;
  margin-left: 0px;
  box-sizing: border-box;
  background: url(../../public/img/Dango.svg) no-repeat center;
  background-size: 128px;
}
</style>