<template>
  <img alt="Vue logo" src="./assets/dog1.jpg">
  <HelloWorld msg="Welcome to Your dog.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
  background: #e3e5e7;
}

img{
  height: 40%;
  width: 40%;
}
</style>
