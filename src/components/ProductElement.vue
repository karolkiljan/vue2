<template>
  <div class="product">
      <h4>{{ product.name }}</h4>
      <h5>Cena: {{ product.price }} zł</h5>
      <p>Opis: {{ product.description }}</p>
  </div>
</template>

<script setup>
defineProps({
    product: {
        type: Object,
        required: true
    }
})
</script>

<style scoped>
.product {
    display: flex;
    flex-direction: column;
    border: 3px solid black;
    padding: 10px;
    height: 90%;
}
</style>
