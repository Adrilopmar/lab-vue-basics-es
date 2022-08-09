<template>
  <nav-bar/>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <footer-component/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import footerComponent from './components/footerComponent.vue'
import navBar from './components/navBar.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    footerComponent,
    navBar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
