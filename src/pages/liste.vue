<template>
    <div class="p-2">
        <h1 class="text-2xl">Page Liste</h1>
        <div v-for="maisons in maisons" :key="maisons.nom">
            <card class="w-1/2" v-bind="maisons"/>
        </div>
    </div>
    </template>

<script setup lang="ts">
    import card from "../components/card.vue";

  const maisons = [{nom:"Maison 1", price:3004, favoris:true, txt:"produit de test", nbbath:2, nbsize:"500 m²", img:"/public/card.jpg"}, {nom:"Maison 2", price:7900, favoris:false, txt:"2ème produit de test", nbbath:4, nbsize:"700 m²", img:"/public/card2.jpg"}, {nom:"Maison 3", price:1006, txt:"Dernier produit de test", nbbath:1, nbsize:"600 m²", img:"/public/card3.jpg"}]
//   import maisons from "../assets/maisons.json";
</script>