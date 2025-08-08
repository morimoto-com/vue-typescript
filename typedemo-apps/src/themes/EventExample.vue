<template>
  <h2>Event</h2>
  <button @click="countUp">+1</button>
  <p>count: {{ count }}</p>
</template>
<script setup lang="ts">
import { computed, ref } from 'vue'
const count = ref(0)
const doubleCount = computed(() => {
  if (count.value > 3) return 100
  return count.value * 2
})
console.log(doubleCount)
function countUp(event: MouseEvent) {
  count.value++
  console.log(event.clientX)
}
</script>

<style scoped></style>
