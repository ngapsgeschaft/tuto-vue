<template>
  <h2>Coucou depuis mon composant!</h2>
  <p>{{ str.toUpperCase() }}</p>
  <p>Le nom de l'instance est {{ name }}</p>
  <p v-html="message"></p>
</template>

<script>
  export default {
    data() {
        return {
            name: "MyInstance",
            str: "Je suis le str de MyInstance",
            message: "<strong>Je suis un message fort</strong>"
        }
    }
  }
</script>

<style>
</style>