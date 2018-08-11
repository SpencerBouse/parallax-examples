<template>
  <div data-relative-input="true" id="metroid-scene">
    <img class="full-img" data-depth="0.8" src='../assets/metroid3.png'>
    <img class="full-img" data-depth="0.6" src='../assets/metroid2.png'>
    <img class="full-img" data-depth="0.2" src='../assets/metroid1.png'>
  </div>
</template>

<script>
import Parallax from 'parallax-js'

export default {
  mounted() {
    var scene = document.getElementById('metroid-scene');
    var metroidParallax = new Parallax(scene, {
      relativeInput: true,
      clipRelativeInput: true,
      limitX: 100,
      limitY: 100,
      scalarX: 2,
      scalarY: 2,
      frictionX: .05,
      frictionY: .05,
      hoverOnly: true,
    });
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #metroid-scene{
    width: fit-content;
    margin: 0 auto;
  }
  .full-img{
    height:100vh;
  }
</style>
