<template>
  <!-- <h2>Coucou depuis mon composant!</h2>
  <p>{{ str.toUpperCase() }}</p>
  <p>Le nom de l'instance est {{ name }}</p>
  <p v-html="message"></p> -->
  <!-- <p>{{ calc(2, 3)}}</p>
  <p>{{ func() }}</p>
  <a v-bind:href="UrlGoogle" target="_blank">Accéder à Google</a>
  <img :src="UrlImage" alt="" /> -->
  <p>Compteur: {{ compteur }}</p>
  <button @click="plus">+</button>
  <button @click="moins">-</button>
</template>

<script>
  export default {
    data() {
        return {
            name: "MyInstance",
           /*  str: "Je suis le str de MyInstance",
            message: "<strong>Je suis un message fort</strong>" */
           /*  nb: 7,
            UrlGoogle: "https://www.google.com",
            UrlImage: "https://picsum.photos/200/300" */
            compteur: 0,
        }
    },
    methods: {
        /* calc(a, b) {
            return a * b;
        },
        func() {
            return this.name + this.nb;
        } */
        plus() {
          this.compteur++;
        },
        moins() {
            this.compteur--;
        }
    }
  }
</script>

<style>
</style>