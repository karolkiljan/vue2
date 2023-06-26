<template>
  <div v-show="state === 'question'">
      Ile masz lat?
      <input v-model="age" type="number"/>
      <button @click="isAbove">Zatwierdź</button>
  </div>
  <div v-show="state === 'above_18'">
      <Products />
      <button @click="back">Powrót</button>
  </div>
  <div v-show="state === 'not_above_18'">
    Nie możesz przejść dalej
    <button @click="back">Powrót</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Products from "@/components/Products.vue";

const age = ref(null)
const state = ref("question")

function isAbove() {
    if (age.value > 18) {
        state.value = "above_18"
    } else {
        state.value = "not_above_18"
    }
}

function back() {
    state.value = "question"
}

</script>

<style scoped>
</style>
