<template>
  <h2>Emit</h2>
  <EmitChildComp @update="onUpdate" />
  <p>count: {{ count }}</p>
</template>

<script setup lang="ts">
import EmitChildComp from '@/components/EmitChildComp.vue'
import { ref } from 'vue'
const count = ref<number>(0)
function onUpdate(value: number) {
  count.value = count.value + value
}
</script>

<style scoped></style>
