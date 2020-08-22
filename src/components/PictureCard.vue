<template>
<div>
    <div v-for="card in Cards" v-bind:key="card.id">
        <Picture 
        :image="card.img"
        />
    </div>
</div>
</template>

<script>
import Picture from './Picture.vue'
export default {

 components: {
    Picture
  },
  data() {
    return {
      Cards : [
        { img: "sea1" },
        { img: "sea2" },
        { img: "sea3" }
      ] 
      }
    }
}
</script>
