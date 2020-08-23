<template>
    
<div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
  
  <div class="carousel-inner" id="img">
      <p>Project-Like</p>
        <div class="carousel-item active">
<!-- Image Slide 01 -->
        <img  class="d-block w-100" src="../assets/img/sea1.jpg" >
        </div>
        <div class="carousel-item" v-for="image in images" :key="image.id" >
<!-- Image Slide -->
            <img v-bind:src="require(`../assets/img/${image.url}`)" class="d-block w-100" alt="...">
        </div>
  </div>
 
  <a  class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a  class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span id="button" class="carousel-control-next-icon" aria-hidden="true"></span>
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

<style>
#img{
  width: 80%;
  background-color: white;
  box-shadow: 0 10px 100px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
 border-radius: 30px;
}
#carouselExampleControls{
  display: flex;
  justify-content: center;
}
#button{
  color: black;
}

</style>