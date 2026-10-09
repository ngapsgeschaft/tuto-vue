<template>
<p>{{ count }}</p>
<button v-on:click="increment">+</button>
<hr>
<p>{{ state.message }}</p>
<button v-on:click="updateMessage">Changer ce message</button>
</template>

<script setup>

import { ref, reactive } from 'vue';

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
</script>

<style>
</style>