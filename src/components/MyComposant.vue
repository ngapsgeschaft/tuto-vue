<template>
  <button @click="addItem">Add Item</button>
  <button @click="removeItem" :disabled="items.length === 0">Remove Item</button>

  <transition-group name="list" tag="ul">
    <li v-for="item in items" :key="item" class="list-item">
      {{ item }}
    </li>
  </transition-group>
</template>

<script setup>
import { ref } from 'vue';

const items = ref([])

let nextId = ref(1)

const addItem = () => {
  items.value.push(`Element ${nextId.value++}`)
}

const removeItem = () => {
  items.value.pop()
}
</script>

<style>
button {
  margin: 5px;
  padding: 10px;
  font-size: 16px;
  cursor:pointer;
}

ul {
  list-style: none;
  padding: 0;
}

.list-item {
  background: crimson;
  color: write;
  padding: 10px;
  margin: 5px;
  border-radius: 5px;
  transition: all 0.5s ease;
}

.list-enter-active, .list-leave-active {
  transition: opacity 0.5s , transform .5s;
}

.list-enter-form, .list-leave-to {
  opacity: 0;
  transform: translateY(-20px);
}
</style>