<template>
  <div>
    <h1>Typescript学習テーマ一覧</h1>
    <ul>
      <li v-for="(component, key) in componentsMap" :key="key" @click="currentTheme = key">
        {{ key }}
      </li>
    </ul>
    <component :is="componentsMap[currentTheme]" />
  </div>
</template>

<script setup lang="ts">
import { ref, markRaw } from 'vue'
import type { Component } from 'vue'

import RefExample from './themes/RefExample.vue'
import ComputedExample from './themes/ComputedExample.vue'

// テーマ名をキーにして、Vueコンポーネントを値に持つマップを定義
const componentsMap: Record<string, Component> = {
  ref: markRaw(RefExample),
  computed: markRaw(ComputedExample),
}

// 現在のテーマを管理するリアクティブ変数
const currentTheme = ref<keyof typeof componentsMap>('ref')
</script>
