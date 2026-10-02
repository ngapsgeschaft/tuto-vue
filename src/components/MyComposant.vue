<template>
  <!-- <h2>Coucou depuis mon composant!</h2>
  <p>{{ str.toUpperCase() }}</p>
  <p>Le nom de l'instance est {{ name }}</p>
  <p v-html="message"></p> -->
  <p>{{ calc(2, 3)}}</p>
  <p>{{ func() }}</p>
</template>

<script>
  export default {
    data() {
        return {
            name: "MyInstance",
           /*  str: "Je suis le str de MyInstance",
            message: "<strong>Je suis un message fort</strong>" */
            nb: 7
        }
    },
    methods: {
        calc(a, b) {
            return a * b;
        },
        func() {
            return this.name + this.nb;
        }
    }
  }
</script>

<style>
</style>