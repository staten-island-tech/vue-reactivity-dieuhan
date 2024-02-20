<template>
    <div>
      <h1 class="header">Shopping Cart</h1>
      <div v-if="cart.length === 0" class="empty-cart">
        Your cart is empty
      </div>
      <div v-else>
        <div v-for="(item, index) in cart" :key="index" class="cart-item">
          <h2>{{ item.title }}</h2>
          <h3>{{ item.artist }}</h3>
          <h4>{{ item.price }}</h4>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const cart = ref([]);
  
  function addToCart(vinyl) {
    cart.value.push(vinyl);
    console.log("Added to cart:", vinyl);
  }

  addToCart();
  </script>
  
  <style scoped>
  .header {
    text-align: center;
    margin-top: 20px;
  }
  
  .empty-cart {
    text-align: center;
  }
  
  .cart-item {
    margin: 1rem auto;
    width: 80%;
    border: 1px solid #ccc;
    padding: 1rem;
  }
  </style>
  