<template>
<p>{{ count }}</p>
<button v-on:click="increment">+</button>
<hr>
<p>{{ state.message }}</p>
<button v-on:click="updateMessage">Changer ce message</button>
<p>{{ doubleCount }}</p>
<hr>
<UserSlot title="Mon Slot">
  <p>Hello from parent</p>
</UserSlot>
</template>

<script setup>

import { ref, reactive, computed, provide, inject } from 'vue';
import UserSlot from './UserSlot.vue';

const count = ref(0);

const increment = () => {
  count.value++;
}

const state = reactive({
  message: "Hello World"
})

const updateMessage = () => {
  state.message = "Bonjour tout le monde";
}

const doubleCount = computed(() => count.value * 2)

provide("count", count);


</script>

<style>
</style>