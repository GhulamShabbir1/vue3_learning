<template>
  <div>
    <h1>{{ message}}</h1>
    <p v-html="tag" ></p>
    <p v-bind:class="objectOfAttrs"> this is Attribute binding</p>
    <button :disabled="true"> Disable me</button>
    <button @click="increment()">Increment</button>
    <p>Count: {{ count }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const count = ref(0);
const message = ref('Hello, Vue 3!');
const tag=ref('<h1>Interpolation Example</h1>');

// const box="container";
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: 'background-color:green'
}

function increment(count){
  count.value++;
}
</script>

<style scoped>
.container {
  background-color: rgb(25, 112, 141);
  padding: 20px;
  border-radius: 5px;
}
</style>