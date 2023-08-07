<template lang="">
<div>
    Component1
    <button @click="awesome = !awesome">Toggle</button>
    <h1 v-if="awesome">Vue is awesome!</h1>
    <h1 v-else>Oh no 😢</h1>
</div>
</template>

<script setup>
import { ref } from 'vue'
const awesome = ref(false);
</script>

<style lang="">
</style>
