<template>
  <h3>EmitChild</h3>
  <button @click="$emit('update', 100)">button</button>
</template>
<script setup lang="ts">
defineEmits<{
  // タプル型で指定
  update: [count: number]
  // update: [number]
}>()
// defineEmits(['update'])
</script>
<style scoped></style>
