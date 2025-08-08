<template>
  <h3>ChildComp</h3>
  <p>title: {{ title }}</p>
</template>

<script setup lang="ts">
// TypeScriptでの書き方（Typeベースデクラレーション）
const { title = 'default course' } = defineProps<{
  title: string
  // requiredはデフォルトでtrue
  // falseにするには "title?: string"
  // defaultは変数の分割代入を用いる
}>()
// JavaScriptでの書き方（ランタイムデクラレーション）
// defineProps({
//   title: {
//     type: String,
//     required: true,
//     default: 'default course',
//   },
// })
</script>
<style scoped></style>
