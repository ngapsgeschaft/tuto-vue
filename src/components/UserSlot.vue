<template>
    <div class="card">
        <h2> {{ title }}</h2>
        <div class="content">
            <slot></slot>
        </div>
        <p>count depuis le parent: {{ count }}</p>
    </div>
</template>

<script setup>
  import { inject } from 'vue';

  defineProps({
    title: String
  })

  const count = inject("count", 0);
</script>

<style>
</style>