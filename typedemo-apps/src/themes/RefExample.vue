<template>
  <h2>Ref</h2>
  <p>count: {{ count }}</p>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const count = ref<number | string>(0)
count.value = 'hello'
</script>

<style scoped></style>
