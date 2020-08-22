<template>
    
<div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner" >
      
        <div class="carousel-item active">
<!-- Image Slide 01 -->
        <img class="d-block w-100" src="../assets/img/sea1.jpg" >
        </div>
        <div class="carousel-item" v-for="image in images" :key="image.id" >
<!-- Image Slide -->
            <img v-bind:src="require(`../assets/img/${image.url}`)" class="d-block w-100" alt="...">
        </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

</template>

<script>
export default {
    data () {
        return {
            images: [
                { url: "sea2.jpg"},
                { url: "sea3.jpg"}
            ]
        }
        }
}
</script>