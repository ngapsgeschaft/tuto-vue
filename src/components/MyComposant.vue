<template>
  <button @click="toggleVisible">toggleElement</button>

  <transition
    @before-enter="beforeEnter"
    @enter="enter"
    @after-enter="afterEnter"
    @leave="leave">
    <p v-if="isVisile">je suis visible</p>
  </transition>
</template>

<script setup>
import { ref } from 'vue'

const isVisile = ref(false)

const toggleVisible = () => {
  isVisile.value = !isVisile.value
}

const beforeEnter = (el) => {
  el.style.opacity = 0
}

const enter = (el, done) => {
  el.offsetHeight
  el.style.transition = "opacity 0.5s ease"
  el.style.opacity = 1
  done() // indique la fin de l'animation
}

const afterEnter = (el) => {
  console.log("afterEnter");
}

const leave = (el, done) => {
  el.offsetHeight
  el.style.transition = "opacity 0.5s ease"
  el.style.opacity = 0
  done() // indique la fin de l'animation
}
</script>

<style>
</style>