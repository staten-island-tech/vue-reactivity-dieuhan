<template>
  <div class="about">
    <h1 class="carthead">Your Cart</h1>
  
  </div>
</template>

<script setup>
import { ref } from 'vue';
import DestCard from '@/components/DestCard.vue';
import HomeView from './HomeView.vue';

</script>

<style>

  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
    text-align: center;
  }

  .carthead{
    text-align: center;
  }

</style>
