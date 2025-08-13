<template>
  <div>
    <h1>{{ message }}</h1>
    <p v-html="tag" ></p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('Hello, Vue 3!');
const tag=ref('<h1>Interpolation Example</h1>');
</script>