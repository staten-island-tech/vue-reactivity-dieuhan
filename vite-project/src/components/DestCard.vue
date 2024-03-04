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
  emits('addToCart', props.Vinyl);
}

</script>

<style scoped>

img{
    width: 300px;
    height: 300px;
}

.card{
<<<<<<< HEAD
margin: 2rem 0;
  width: 26%;
  height: auto;
=======
    height: 50vh;
  margin: 2rem 0;
  width: 28%;
>>>>>>> parent of ea6e1e0 (bleepbloop)
  display: flex;
  flex-direction: column;
  align-items: center;
}

.bb{
    margin-top: 20px;
}



</style>