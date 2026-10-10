<template>
  <h2>Liste des utilisateurs</h2>

  <div v-if="loading">Chargement...</div>

  <div v-if="error">Erreur: {{ error }}</div>

  <ul v-if="users.length">
    <li v-for="user in users" :key="user.id">
      {{ user.name }}
    </li>
  </ul>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import axios from 'axios';

const users = ref([]);
const loading = ref(false)
const error = ref(null)

const fetchUsers = async () => {
  loading.value = true
  error.value = null

  try{
    const response = await axios.get('https://jsonplaceholder.typicode.com/users')
    users.value = response.data
  } catch(e) {
    error.value = e.message
  } finally {
    loading.value = false
  }
}

onMounted(fetchUsers)
</script>

<style>
</style>