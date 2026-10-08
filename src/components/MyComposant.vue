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
  <!-- <div>
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
    <p>Status computed: {{ statusComputed }}</p>
  </div> -->
  <!-- <div class="box"></div>
  <div v-bind:style="inlineStyle">Ce texte a du CSS inline.</div>
  <div class="box-style"></div>
  <div class="box-style-2"></div> -->
<!-- 
  <p class="text-blue-500 bg-green-100 py-2 px-4">Hello</p> -->

  <!-- Chapitre 03 - Les conditions
  <h1 v-if="status === 'success'">Succès</h1>
  <h1 v-else-if="status === 'warning'">Avertissement</h1>
  <h1 v-else="status === 'error'">Erreur</h1>

  <button v-on:click="changeStatus('success')">Success</button>
  <button v-on:click="changeStatus('warning')">Warning</button>
  <button v-on:click="changeStatus('error')">Error</button> -->

  <!-- Chapitre 03 - La boucle v-for
  <h2>Liste des fruits</h2>
  <ul>
    <li v-for="(fruit, index) in fruits" :key="index">
      {{ fruit }}
    </li>
  </ul>
  
  <h2>Liste des utilisateurs</h2>
  <ul>
    <li v-for="(user, index) in users" :key="index">
      {{ user.name }} - {{ user.age }}
    </li>
  </ul>

  <h2>Liste des équipes</h2>
  <ul>
    <li v-for="(team, teamIndex) in teams" :key="teamIndex">
      <span class="text-red-600">{{ team.name }}</span>
      <ul>
        <li v-for="(member, memberIndex) in team.members" :key="memberIndex">
          {{ member }}
        </li>
      </ul>
    </li>
  </ul> -->

  <!-- <user-card v-for="(user, index) in users" :key="index" :user="user"/> -->
  <h2>{{ title || "Titre depuis le parent"}}</h2>
  <p>{{ description || "Description depuis le parent" }}</p>
  <user-card v-on:update-title="updateTitle" @update-description="updateDescription"/>

  <UserSlot title="Mon titre depuis le parent">
    <p>Contenu du slot depuis le parent</p>
  </UserSlot>
</template>

<script setup>
import UserCard from './UserCard.vue';
import UserSlot from './UserSlot.vue';

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
  /* export default {
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
    },
    computed: {
      statusComputed() {
        return this.compteurA > 10 ? 'Supérieur à 10': 'Inférieur à 10';
      }
    },
    watch: {
      compteurA(newValue, oldValue) {
        console.log(`CompteurA incrémenté: actuel ${newValue}; précédent: ${oldValue}`);
        
      }
    }
  } */

  /* export default {
    data() {
      return {
        inlineStyle: {
          color: "yellow",
          fontSize: "25px",
        }
      }
    }
  } */
  
  /* // Chapitre 03 - Les conditions
  export default {
    data () {
      return {
        status: 'error',
      }
    },
    methods: {
      changeStatus(newStatus) {
        this.status = newStatus;
      }
    }
  } */

  /* // Chapitre 03 - La boucle v-for
  export default {
    data () {
      return {
        fruits: ['Pomme', 'Banane', 'Orange', 'Fraise'],
        users: [
          { id: 1, name: 'Alice', age: 25 },
          { id: 2, name: 'Bob', age: 30 },
          { id: 3, name: 'Charlie', age: 35 }
        ],
        teams: [
          { id: 1, name: 'Team A', members: ['Alice', 'Bob'] },
          { id: 2, name: 'Team B', members: ['Charlie', 'David'] },
          { id: 3, name: 'Team C', members: ['Eve', 'Frank'] }
        ]
      }
    }
  } */

//   export default {
//     name: 'MyComposant',
//     components: {
//       UserCard
//     },
//     data() {
//       return {
//         /* users: [
//           { id: 1, name: 'Alice', age: 25 },
//           { id: 2, name: 'Bob', age: 30 },
//           { id: 3, name: 'Charlie', age: 35 }
//         ] */
//         title: "",
//         description: ""
//       }
//     },
//     methods: {
//       updateTitle(newTitle) {
//         this.title = newTitle;
//       },
//       updateDescription(newDescription) {
//         this.description = newDescription;
//       }
//     }
//   }
// </script>

<!-- <style scoped src="../assets/styles/mystyle2.css">
.box {
  width: 200px;
  height: 200px;
  background-color: green;
}
</style> -->
<style>
</style>