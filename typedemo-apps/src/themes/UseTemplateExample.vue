<template>
  <h2>UseTemplateRef</h2>
  <input ref="user-input" type="text" />
</template>

<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue'
// useTemplateRefは方推論は任せればよい
const userInput = useTemplateRef('user-input')
onMounted(() => {
  userInput.value?.focus()
})
</script>

<style scoped></style>
