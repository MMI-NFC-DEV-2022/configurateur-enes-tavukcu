<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import BasketDessus from './components/BasketDessus.vue';
import BasketProfil from './components/BasketProfil.vue';
import FormBasket from './components/FormBasket.vue';

</script>

<template>
  <h1 class="bg-red-500">
    <RouterLink to="/about">About</RouterLink>
  </h1>
  <FormSvg />
</template>

