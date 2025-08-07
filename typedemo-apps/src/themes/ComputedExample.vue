<template>
  <h2>computed</h2>
  <p>count:{{ count }}</p>
  <p>doubleCount:{{ doubleCount }}</p>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
const count = ref(1)
const doubleCount = computed(() => {
  if (count.value > 3) return 100
  return count.value * 2
})
</script>

<style scoped></style>
