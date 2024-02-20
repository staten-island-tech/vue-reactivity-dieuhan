<template>
        <div class="card" >
            <h2>{{ Vinyl.title }}</h2>
        <h3>{{Vinyl.artist}}</h3>
        <h4>{{Vinyl.price}}</h4>
        <img :src="Vinyl.img" alt=""/>
        <h5>{{ clicked }}</h5>
        <button @click="increment">Add to Cart</button>
        </div>
        
   
</template>

<script setup>
import{ defineProps, ref } from "vue";
const props = defineProps({
    Vinyl: Object, 
});

//clicker logic
const clicked = ref(0);
function increment(){
    clicked.value++;
}


</script>

<style scoped>

img{
    width: 300px;
    height: 300px;
}

.card{
    height: 50vh;
  margin: 2rem 0;
  width: 28%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

</style>