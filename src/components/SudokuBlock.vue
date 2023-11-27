<script setup lang="ts">
import { computed, ref } from 'vue'
import type NumberBlockVue from './NumberBlock.vue'

const number = ref(4)
const isGreaterThanText = computed(() => {
  if (number.value > 5) {
    return 'greater than 5'
  }
  return 'less than 5'
})
</script>

<template>
  <div class="sudoku-block">
    {{ number }}
    <NumberBlockVue v-for="n in 9" :key="n"> </NumberBlockVue>
  </div>
</template>

<style scoped>
div {
  border: 1px solid red;
}
</style>
