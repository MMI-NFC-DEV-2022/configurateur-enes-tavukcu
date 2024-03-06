<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router/auto';
import BasketDessus from './components/BasketDessus.vue';
import BasketProfil from './components/BasketProfil.vue';
import FormBasket from './components/FormBasket.vue';

</script>

<template>
  <header>
  <h1 class="bg-red-500 p-5 text-white uppercase text-center ">
    La boutique d'Enes
  </h1>
  <h1 class="bg-red-500 p-5">
    <RouterLink to="/" class="p-10">Home</RouterLink>
    <RouterLink to="/about" class="p-10">About</RouterLink>
    <RouterLink to="/basket/exemple/1" class="p-10">Basket Exemple</RouterLink>
    <RouterLink to="/basket/edit/1" class="p-10">Basket Edit</RouterLink>
    

  </h1>
  </header>

<RouterView />
  <main>
   
  </main>
</template>

