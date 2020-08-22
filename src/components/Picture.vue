<template>
 <div class="container" id="picture">
     <div class="card">
          <p class="card-text 
                    d-flex justify-content-end 
                    p-3">
                Counter: {{counter}}
            </p>
<!-- Image -->
            <img 
                :src="require(`../assets/img/${image}.jpg`)"
                class="card-img-top mx-auto picture" 
                style="width:400px">

        <div class="card-body">
<!-- Couter -->
           
        </div>
<!-- Button footer -->
        <div class="d-flex justify-content-center">
            <ul class="list-inline">
            <li v-for="btn in buton" 
                v-bind:key="btn.id" 
                class="list-inline-item">
                <ButtonAction 
                    :data = "btn.name" 
                    :couter = btn.couter
                    v-on:toParent="onClick"
                    />
            </li>
            </ul>
        </div>
<!-- end button footer -->
     </div>
 </div> 
</template>

<script>
import ButtonAction from './Button'

export default {
    components: {
        ButtonAction
        },
    data () {
        return {
            buton : [
                { name:"like", couter:1 },
                { name:"love", couter:10},
                { name:"haha", couter:5},
                { name:"wow", couter:20},
                { name:"sad", couter:-5},
                { name:"angry", couter:-20}
                ],
            counter:0
        }
    },
    props : ['image'],
    methods: {
        onClick (value) {
            this.counter = this.counter + value
            }
        }
}
</script>

<style>

#picture{
    padding: 20px;
    }
.picture {
    border-radius: 20px;
    }

</style>