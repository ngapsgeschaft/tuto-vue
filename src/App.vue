<script>
import MyComposant from './components/MyComposant.vue';

export default {
  components: {
    MyComposant
  },
  methods: {
    callChild() {
      this.$refs.child.someFunc()
    }
  }
}
</script>

<template>
  <h1>Hello, World!</h1>
  <my-composant ref="child"></my-composant>

  <button @click="callChild">Appeler function</button>
</template>

<style scoped>
h1 {
  color: red;
}
</style>
