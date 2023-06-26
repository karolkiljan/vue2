<template>
  <li>
      <ul v-for="product in products"><ProductElement :product="product" /></ul>
  </li>
</template>

<script setup>
import { ref } from 'vue'
import ProductElement from "@/components/ProductElement.vue";

const products = ref([
    {
        "name": "Kawa",
        "description": "Super kawa do picia",
        "price": 29.95
    },
    {
        "name": "Sok cytrynowy",
        "description": "Pół litra nektaru",
        "price": 9.95
    },
    {
        "name": "Lays",
        "description": "Chipsy przepyszne paprykowe",
        "price": 6.95
    },
    {
        "name": "Czekolada",
        "description": "Czarna czekolada",
        "price": 9.95
    },
    {
        "name": "Truskawki",
        "description": "Pyszne niepryskane truskawki",
        "price": 36.95
    }
])
</script>

<style scoped>
ul, li {
    list-style: none;
}

li {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: stretch;
}

ul {
    padding: 5px;
    flex: 1;
}
</style>
