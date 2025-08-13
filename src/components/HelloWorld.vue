<template>
  <div>
    <h1>{{ message }}</h1>
    <p v-html="tag" ></p>
    <p v-bind:class="box"> this is Attribute binding</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('Hello, Vue 3!');
const tag=ref('<h1>Interpolation Example</h1>');
const box="container";
</script>

<style scoped>
.container {
  background-color: rgb(25, 112, 141);
  padding: 20px;
  border-radius: 5px;
}
</style>