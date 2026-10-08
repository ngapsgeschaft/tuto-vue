<template>
    <div class="user-card">
        <!-- <h3>{{ user.name }}</h3>
        <p>Age: {{ user.age }}</p> -->
        <input v-on:input="dataToParent" v-model="title" placeholder="Entrez un titre" />
        <input v-on:input="dataToParent" v-model="description" placeholder="Entrez une description" />
        <!-- <button v-on:click="dataToParent">Envoyer au parent</button> -->
    </div>
</template>

<script>

  export default {
    name: "UserCard",
    /* props: {
      user: Object
    } */
    data() {
        return {
            title: "",
            description: ""
        }
    },
    methods: {
        dataToParent() {
            this.$emit('update-title', this.title);
            this.$emit('update-description', this.description);
        }
    }
  }

</script>

<style scoped>
  .user-card {
    border: 1px solid #ebe5e5;
    padding: 10px;
    margin: 10px;
    box-shadow: 0 2px 5px rgba(239, 237, 231, 0.1);
  }
</style>