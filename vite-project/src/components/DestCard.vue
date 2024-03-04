<template>
        <div class="card" >
            <h2>{{ Vinyl.title }}</h2>
        <h3>{{Vinyl.artist}}</h3>
        <h4>{{Vinyl.price}}</h4>
        <img :src="Vinyl.img" alt=""/>
        
        <button class="bb" @click="addToCart">Add to Cart</button>
        </div>
        
   
</template>

<script setup>
import{ defineProps, defineEmits } from "vue";


const props = defineProps({
    Vinyl: Object, 
});

//clicker logic
/* const clicked = ref(0);
function increment(){
    clicked.value++;
} */

const emits = defineEmits(['addToCart']);

function addToCart() {
  emits('addToCart', props.Vinyl); //create or "emit" addtocart
}

</script>

<style scoped>

h2, h3, h4{
    margin: 0.5rem;
}

img{
    width: 100%;
    height: auto;
}

.card{
  border: 1PX solid black;
  margin: 5%;
  width: 28%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bb{
    margin-top: 20px;
}



</style>