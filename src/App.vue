<template>
  <div  id="app" 
        class="container">
    <Slider />
    <PictureCard />
  </div>
</template>

<script>
import Slider from './components/Slider.vue'
import PictureCard from './components/PictureCard.vue'

export default {
  name: 'App',
  components: {
    PictureCard,
    Slider
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
