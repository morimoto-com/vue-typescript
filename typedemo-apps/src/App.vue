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
import type { Component } from 'vue'
import { markRaw, ref } from 'vue'

import ComputedExample from './themes/ComputedExample.vue'
import EventExample from './themes/EventExample.vue'
import PropsExample from './themes/PropsExample.vue'
import RefExample from './themes/RefExample.vue'
import UseTemplateExample from './themes/UseTemplateExample.vue'

// テーマ名をキーにして、Vueコンポーネントを値に持つマップを定義
const componentsMap: Record<string, Component> = {
  ref: markRaw(RefExample),
  computed: markRaw(ComputedExample),
  useTemplate: markRaw(UseTemplateExample),
  event: markRaw(EventExample),
  props: markRaw(PropsExample),
}

// 現在のテーマを管理するリアクティブ変数
const currentTheme = ref<keyof typeof componentsMap>('ref')
</script>
