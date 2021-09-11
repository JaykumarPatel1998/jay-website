<template>
  <h1>Jaykumar Patel</h1>
  <LandingPage/>
</template>

<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: "App",
  components: {
    LandingPage,
  },
  data(){
    return{
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 100%;
}

h1{
  margin: 20px auto;
  width: 65%;
  color: rgb(206, 29, 197);
  background: black;
  padding: 10px;
  border-radius: 5px;
}

</style>
