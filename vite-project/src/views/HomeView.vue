<template>
  <div>
<h1 class="header">uhans vinyl shop :D </h1>

    <div class="gallery">
    <DestCard v-for="vinyl in vinyls" 
    :key="vinyl.title"
    :Vinyl="vinyl"/>
  </div>
</div>
</template>

<script setup>
import DestCard from '@/components/DestCard.vue';

const vinyls = [
        {
          title: "uncounted 0.00",
          artist: "wave to earth",
          price: "$59.99",
          img: "https://i.scdn.co/image/ab67616d0000b27384e864c4464946acecf15f9c",
        },
        {
          title: "Immunity",
          artist: "Clairo",
          price: "$25.00",
          img: "https://m.media-amazon.com/images/I/81yJk22VcSL._UF1000,1000_QL80_.jpg",
        },
        {
          title: "When We Were Friends",
          artist: "The Backseat Lovers",
          price: "29.87",
          img: "https://i.scdn.co/image/ab67616d0000b2738386795a636d72e74c958590"
        },
        {
          title: "emails i can't send",
          artist: "Sabrina Carpenter",
          price: "$25.99",
          img: "https://cdn11.bigcommerce.com/s-1xa2dhlu0a/images/stencil/1280x1280/products/144352/158575/LDC67062___95270.1666108786.jpg?c=1",
        },
        {
          title: "Nothing Happens",
          artist: "Wallows",
          price: "22.99",
          img: "https://m.media-amazon.com/images/I/818UcoZySEL._UF1000,1000_QL80_.jpg",
        },
        {
          title: "Fine Line",
          artist: "Harry Styles",
          price: "$30.49",
          img: "https://m.media-amazon.com/images/I/61TZoz02rbL._UF1000,1000_QL80_.jpg",
        },
        {
          title: "GUTS",
          artist: "Olivia Rodrigo",
          price: "$27.50",
          img: "https://upload.wikimedia.org/wikipedia/en/thumb/0/03/Olivia_Rodrigo_-_Guts.png/220px-Olivia_Rodrigo_-_Guts.png",
        },
        {
          title: "folklore",
          artist: "Taylor Swift",
          price: "$29.98",
          img: "https://m.media-amazon.com/images/I/A1Q6XGXmIFL._UF1000,1000_QL80_.jpg"
        },
        {
          title: "Wiped Out!",
          artist: "The Neighbourhood",
          price: "$46.16",
          img: "https://i.ebayimg.com/images/g/6NsAAOSwAiRih285/s-l1200.webp"
        },
        {
          title: "minor",
          artist: "Gracie Abrams",
          price: "$27.98",
          img: "https://m.media-amazon.com/images/I/61Yv2sYgeIL._UF1000,1000_QL80_.jpg"
        },
        {
          title: "Selfish Machines",
          artist: "Pierce The Veil",
          price: "$55.99",
          img: "https://m.media-amazon.com/images/I/81+NpLULLKL._UF1000,1000_QL80_.jpg"
        },
        {
          title: "The Bends",
          artist: "Radiohead",
          price: "$33.09",
          img: "https://upload.wikimedia.org/wikipedia/en/5/55/Radioheadthebends.png"
        },
        {
          title: "AM",
          artist: "Arctic Monkeys",
          price: "$23.99",
          img: "https://m.media-amazon.com/images/I/51B3GKIqOFL._UF1000,1000_QL80_.jpg"
        },
        {
          title: "French Exit",
          artist: "TV Girl",
          price: "$35.43",
          img: "https://i.scdn.co/image/ab67616d0000b273e1bc1af856b42dd7fdba9f84"
        },
        {
          title: "Superache",
          artist: "Conan Gray",
          price: "$39.98",
          img: "https://m.media-amazon.com/images/I/91Z3q2ceS-L._UF1000,1000_QL80_.jpg"
        },
      ]


</script>

<style scoped>

.header{
  text-align: center;
  margin-top: 20px;
}
.gallery{
  margin: 1rem auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 80vw;
}

</style>




