<template>
<p>{{ count }}</p>
<button v-on:click="increment">+</button>
</template>

<script setup>

import { ref } from 'vue';

const count = ref(0);

const increment = () => {
  count.value++;
}

</script>

<style>
</style>