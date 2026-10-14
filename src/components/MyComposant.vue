<template>
  <button v-for="tab in Object.keys(tabComponents)" :key="tab" @click="currentTab = tab" :class="{active: currentTab === tab}">
    {{ tab }}
  </button>

  <keep-alive :max="2" :include="['Tab1', 'Tab2']" :exclude="[]">
    <component :is="currentTabComponent"/>
  </keep-alive>
</template>

<script setup>
import { ref, computed } from 'vue'
import Tab1 from './Tab1.vue'
import Tab2 from './Tab2.vue'

const currentTab = ref(Tab1)

const tabComponents = {
  Tab1,
  Tab2
}

const currentTabComponent = computed(() => tabComponents[currentTab.value])
</script>

<style>
button.active {
  background: crimson;
}
</style>