<script setup lang="ts">
import type { Basket } from "@/types";
import { ref } from "vue";
import { FormKit }  from "@formkit/vue";
import BasketProfil from "./BasketProfil.vue";
import BasketDessus from "./BasketDessus.vue";
import  { colors } from "@/types";

const props = defineProps<{
  data?: Basket;
  id?: string;
}>();

const chaussure = ref<Basket>(props.data ?? {});

</script>
<template>

<div class="p-2">

<ul class="flex gap-1">
    <li><a href="#profil">Profil</a></li>
    <li><a href="#dessus">Dessus</a></li>
</ul>

<div class="carousel w-64">
<BasketProfil class="carousel-item w-64" v-bind="chaussure" id="profil" />
<BasketDessus class="carousel-item w-64" v-bind="chaussure" id="dessus"/>
</div>

<FormKit type="form" v-model="chaussure">
<FormKit name="semelle" label="SEMELLE" value="#000000" type="radio" :options="colors"/>
<FormKit name="empeigne" label="EMPEIGNE" value="#FFFFFF" type="radio" :options="colors" />
<FormKit name="pointe" label="POINTE" value="#FFFFFF" type="radio" :options="colors" />
<FormKit name="oeillet" label="OEILLET" value="#FFFFFF" type="radio" :options="colors" />
<FormKit name="bande" label="BANDE" value="#FFFFFF" type="radio" :options="colors" />
<FormKit name="languette" label="LANGUETTE" value="#000000" type="radio" :options="colors" />
<FormKit name="lacet" label="LACET" value="#FFFFFF" type="radio" :options="colors" />
<FormKit name="trimestre" label="TRIMESTRE" value="#FFFFFF" type="radio" :options="colors" />
</FormKit>
</div>
</template>