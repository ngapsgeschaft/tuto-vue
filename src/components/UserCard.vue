<template>
    <div class="user-card">
        <h3>{{ user.name }}</h3>
        <p>Age: {{ user.age }}</p>
    </div>
</template>

<script>

  export default {
    name: "UserCard",
    props: {
      user: Object
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