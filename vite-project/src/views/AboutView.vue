<template>
  <div class="about">
    <h1 class="carthead">Your Cart</h1>
    <ul>
      <li v-for="item in cart" :key="item.title">
        {{ item.title }} - {{ item.price }}
      </li>
    </ul>
    <p>Total Price: {{ totalPrice }}</p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const cart = ref([]);

const totalPrice = computed(() => {
  return cart.value.reduce((total, item) => total + parseFloat(item.price.replace('$', '')), 0).toFixed(2);
});
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
  }

  .carthead{
    text-align: center;
  }
}
</style>
