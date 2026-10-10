<template>
  <button @click="toggleVisible">Toggle element</button>
  <transition name="fade">
    <p v-if="isVisible">je suis un element</p>
  </transition>
</template>

<script setup>
import { ref } from 'vue';

const isVisible = ref(false);

const toggleVisible = () => {
  isVisible.value = !isVisible.value;
}
</script>

<style>
.fade-enter-active, .fade-leave-active {
  transition: opacity 1s ease;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>