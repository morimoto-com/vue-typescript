<template>
    <h2>Define Model</h2>
    <DefineChildComp v-model="userInput"/>
    <p>userInput: {{ userInput }}</p>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import DefineChildComp from '@/components/DefineChildComp.vue';
const userInput = ref('')
</script>

<style scoped>

</style>