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
  <h1 class="bg-red-500 p-5 flex justify-center ">
    <RouterLink to="/" class="p-10 hover:text-red-50">Home</RouterLink>
    <RouterLink to="/about" class="p-10 hover:text-red-50">About</RouterLink>
    <RouterLink to="/basket" class="p-10 hover:text-red-50">Basket</RouterLink>
    <RouterLink to="/basket/edit/1" class="p-10 hover:text-red-50">Basket Edit</RouterLink>
    

  </h1>
  </header>
<Suspense>
<RouterView />
</Suspense>
  <main>
   
  </main>
</template>

