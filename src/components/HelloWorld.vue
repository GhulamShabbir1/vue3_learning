<template>
  <div>
    <h1>{{ message }}</h1>
    <p>This is a simple Vue 3 component.</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const message = ref('Hello, Vue 3!');
</script>