<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
<!--   <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
     

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header> -->
  <nav>
    
    <RouterLink to="/">Shop</RouterLink>
    <RouterLink to="/about">Cart</RouterLink>
 
  </nav>
  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}



  nav {
    text-align: centerS;
    margin-left: -10rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }

</style>
