<script setup lang="ts">
import BasketProfil from "@/components/BasketProfil.vue";
import type { Basket } from "@/types";
import { supabase } from "@/supabase";
console.log("supabase :", supabase);

const exemples: Basket[] = [
    {
        semelle: "#FFFFFF",
        empeigne: "#FFFFFF",
        pointe: "#FFFFFF",
        oeillet: "#FFFFFF",
        bande: "#FFFFFF",
        languette: "#FFFFFF",
        lacet: "#FFFFFF",
        trimestre: "#FFFFFF",
    },

    {
        semelle: "#FFFFFF",
        empeigne: "#FFFFFF",
        pointe: "#FFFFFF",
        oeillet: "#FFFFFF",
        bande: "#FFFFFF",
        languette: "#FFFFFF",
        lacet: "#FFFFFF",
        trimestre: "#FFFFFF",
    },
];
</script>
<template>
  <section>
    <h1 class="text-2xl">Exemples de Baskets</h1>
    <div class="flex flex-wrap gap-2">
      <div class="w-64">
        <RouterLink
        v-for="(exemple, index) in exemples" :key="index"
          :to="{
            name: '/basket/exemple/[data]',
            params: { data: JSON.stringify(exemple) },
          }"
        >
        <BasketProfil class="w-64" v-bind="exemple" />
        </RouterLink>
      </div>
    </div>
  </section>
</template>