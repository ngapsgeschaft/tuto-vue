<template>
  <!-- <h2>Coucou depuis mon composant!</h2>
  <p>{{ str.toUpperCase() }}</p>
  <p>Le nom de l'instance est {{ name }}</p>
  <p v-html="message"></p> -->
  <!-- <p>{{ calc(2, 3)}}</p>
  <p>{{ func() }}</p>
  <a v-bind:href="UrlGoogle" target="_blank">Accéder à Google</a>
  <img :src="UrlImage" alt="" /> -->
  <!-- <p>Compteur: {{ compteur }}</p>
  <button v-on:click="plus">+</button>
  <button @click="moins">-</button> -->
  <!-- <button @:click.once="func">Cliquer ici</button>
  <div @:click="func">
    <button @:click.stop="func">Cliquer ici (stop)</button>
  </div>
  <form @submit.prevent="onSubmit">
    <label for="txt">Texte</label>
    <input type="text" id="txt">
    <button>Envoyer</button>
  </form> -->

  <!-- <input type="text" id="text" v-model="valeur">
  <p>{{ valeur }}</p> -->
  <div>
    <h2>Composant enfant</h2>

    <button v-on:click="compteurA++">+</button>
    <button v-on:click="compteurA--">-</button>
    <p>Valeur compteur A : {{ compteurA }}</p>

    <hr>

    <button v-on:click="compteurB++">+</button>
    <button v-on:click="compteurB--">-</button>
    <p>Valeur compteur B : {{ compteurB }}</p>

    <hr>

    <p>Methode: {{ statusMethod() }}</p>
  </div>
  
</template>

<script>
  // export default {
  //   data() {
  //       return {
           /*  name: "MyInstance", */
           /*  str: "Je suis le str de MyInstance",
            message: "<strong>Je suis un message fort</strong>" */
           /*  nb: 7,
            UrlGoogle: "https://www.google.com",
            UrlImage: "https://picsum.photos/200/300" */
            /* compteur: 0, */
    //     }
    // },
    // methods: {
        /* calc(a, b) {
            return a * b;
        },
        func() {
            return this.name + this.nb;
        } */
        /* plus() {
          this.compteur++;
        },
        moins() {
            this.compteur--;
        } */
     /*  func() {
        console.log('Hello World')
      },
      onSubmit() {
        console.log('Formulaire soumis');
      } */
  //   }
  // }

  /* import {ref} from "vue";

  const valeur = ref(''); */
  
  /* export default {
    methods: {
      someFunc() {
        alert('Fonction du composant enfant appelée');
      }
    }
  } */
  export default {
    data () {
      return {
        compteurA: 0,
        compteurB: 0
      }
    },
    methods: {
      statusMethod() {
        return this.compteurA > 10 ? 'Supérieur à 10': 'Inférieur à 10';
      }
    }
  }
</script>

<style>
</style>