<template>
  <h3>DifineChild</h3>
  <input v-model="model" type="text" />
  <p>model: {{ model }}</p>
</template>
<script setup lang="ts">
// TypeScriptでの書き方（Typeベースデクラレーション）
const [model, modifiers] = defineModel<string, 'trim' | 'uppercase'>({ required: true })
console.log(modifiers.uppercase)
// JavaScriptでの書き方（ランタイムデクラレーション）
// defineModel({ type: String, required: true })
</script>
<style scoped></style>
