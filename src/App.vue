<template>
  <div id="app">
    <SuperMetroid msg="Super Metroid Parallax"/>
  </div>
</template>

<script>
import SuperMetroid from './components/SuperMetroid.vue'

export default {
  name: 'app',
  components: {
    SuperMetroid
  }
}
</script>

<style>
  body{
    background-color: black;
  }
</style>
