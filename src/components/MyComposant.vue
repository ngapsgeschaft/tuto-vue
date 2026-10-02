<template>
  <h2>Coucou depuis mon composant!</h2>
  <p>{{ str }}</p>
  <p>Le nom de l'instance est {{ name }}</p>
</template>

<script>
  export default {
    data() {
        return {
            name: "MyInstance",
            str: "Je suis le str de MyInstance"
        }
    }
  }
</script>

<style>
</style>