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