<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <AppClassbinding />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AppClassbinding from './components/AppCLassbinding.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    AppClassbinding
  }
}
</script>


