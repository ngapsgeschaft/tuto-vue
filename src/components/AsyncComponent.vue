<template>
<h2>Données chargées</h2>
<p>{{  message }}</p>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const message = ref(null)

onMounted(async () => {
    await new Promise((resolve) => setTimeout(resolve, 2000))
    message.value = "Voici les données chargées depuis le serveur"
})
</script>

<style></style>