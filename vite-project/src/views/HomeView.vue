<template>
  <div class="body">
<h1 class="header">uhans vinyl shop :D </h1>

<div class="content">
  <div class="side">
    <div class="gallery">
    <DestCard v-for="vinyl in vinyls" 
    :key="vinyl.title"
    :Vinyl="vinyl"
    @addToCart="addToCart"/>
  </div>

  <div class="cart">
    <h2>Cart</h2>
        <div v-for="item in cart" :key="item.title" class="cart-item">
          <p>{{ item.title }}</p>
          <p>{{ item.price }}</p>
        </div>
        <div class="total">
          <p>Total: ${{ total }}</p>
        </div>
      </div>
    </div>
  </div>
 
 
</div>
</template>

<script setup>
import DestCard from '@/components/DestCard.vue';
import { ref } from 'vue';



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
          price: "$29.87",
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
          price: "$22.99",
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
          img: "https://upload.wikimedia.org/wikipedia/en/1/15/The_Neighbourhood_-_Wiped_Out.jpg"
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
        {
          title: "Girlfriend",
          artist: "The Driver Era",
          price: "$36.60",
          img: "https://m.media-amazon.com/images/I/81CN3Fszm4L._UF1000,1000_QL80_.jpg"
        },
        {
          title: "Beatopia",
          artist: "Beabadoobee",
          price: "$42.00",
          img: "https://media.pitchfork.com/photos/623a9d636597466fa9d6e2ba/master/w_1280%2Cc_limit/beabadoobee-Beatopia.jpg"
        },
        {
          title: "Little Angel",
          artist: "Role Model",
          price: "$17.06",
          img: "https://i.discogs.com/eOz_gWD5HogcgM_uUkwmQjxX5VA13ZhBr-yhuejExyc/rs:fit/g:sm/q:90/h:500/w:500/czM6Ly9kaXNjb2dz/LWRhdGFiYXNlLWlt/YWdlcy9SLTE3MzYx/ODg2LTE2MTMwNDEz/ODQtMzUzMi5qcGVn.jpeg"
        }
      ]

const cart = ref([]);
const total = ref(0);

function addToCart(vinyl) {
  cart.value.push(vinyl);
  console.log('Added to Cart:', vinyl)
  total.value += parseFloat(vinyl.price.replace('$', '')) //add to total 
  total.value = Math.round(total.value * 100) / 100; //round 
}

</script>

<style scoped>

.header{
  text-align: center;
  margin-top: 20px;
}
.gallery{
  
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 80vw;
  background-color: rgb(174, 219, 186);
 margin-left: 90px;
  
}

.cart {
  width: 300px; 
  flex-direction: column;
  margin-left: 60px;

  
}

.cart-item {
  justify-content: space-between;
}

.total {
  margin-top: 20px;
  font-weight: bold;
}

.content {
  display: flex;
  justify-content: center;
}

.side {
  display: flex;
  align-items: flex-start; 
}

</style>




