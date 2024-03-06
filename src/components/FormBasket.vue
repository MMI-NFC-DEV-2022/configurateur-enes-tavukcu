<script setup lang="ts">
import type { Basket } from "@/types";
import { ref } from "vue";
import { FormKit }  from "@formkit/vue";
import BasketProfil from "./BasketProfil.vue";
import BasketDessus from "./BasketDessus.vue";
import  { colors } from "@/types";
import { materiaux } from "@/types";

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
<FormKit 

name="semelle" 
label="SEMELLE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="pointe" 
label="POINTE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
    
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"

    />
    
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="empeigne" 
label="EMPEIGNE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="oeillet" 
label="OEILLET" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="bande" 
label="BANDE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="languette" 
label="LANGUETTE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="lacet" 
label="LACET" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>

<FormKit 

name="trimestre" 
label="TRIMESTRE" 
value="#000000" 
type="radio" 
:options="colors"
:sections-schema="{
    inner: { $el: null },
    decorator: { $el: null },
}"
input-class="peer sr-only"
options-class="flex items-center gap-2"

>
<template #label="context">
    <div
        class="h-6 w-6 rounded-full border-2 peer-checked:border-red-600"
        :style="{ backgroundColor: context.option.value }"
    />
    <span class="sr-only">{{ context.option.value }}</span>
</template>
</FormKit>


</FormKit>
</div>

</template>

