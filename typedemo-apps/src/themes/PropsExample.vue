<template>
  <h2>Props</h2>
  <ChildComp :title="courseTitle" />
</template>

<script setup lang="ts">
import ChildComp from '@/components/ChildComp.vue'
import { ref } from 'vue'
const courseTitle = ref('Vue.js course')
</script>
<style scoped></style>
