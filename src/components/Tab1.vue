<template>
    <div>
        <h2>Tab 1</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque laboriosam veniam reprehenderit at error odit.</p>
        <button @click="increment">{{ count }}</button>
    </div>
</template>

<script setup>
import { ref, onActivated, onDeactivated} from 'vue'

const count = ref(0)

const increment = () => {
    count.value++
}

onActivated(() => {
    console.log('Tab1 activated');
})

onDeactivated(() => {
    console.log('Tab1 dectivate');
})
</script>

<style></style>