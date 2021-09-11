<template>
  <img class="display-picture" src="./assets/jay.jpg" alt="" srcset="">
  <h1 class="namespace">&lt; Jaykumar Patel /&gt;</h1>
  <LandingPage />
</template>

<script>
import LandingPage from "./components/LandingPage.vue";
import gsap from "gsap";
const tl = gsap.timeline({ ease: "SteppedEase.config(55)" });

export default {
  name: "App",
  components: {
    LandingPage,
  },
  data() {
    return {};
  },
  mounted: function () {
   
    tl.fromTo(
      ".namespace",
      {
        width: "0",
      },
      {
        duration: 4,
        width: "75%",
      }
    );
  },
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

h1 {
  white-space: nowrap;
  overflow: hidden;
  box-sizing: content-box;
  margin: 20px auto;
  width: 0;
  color: rgb(206, 29, 197);
  padding: 10px;
  border-radius: 5px;
}

.display-picture{
  max-width: 20%;
  border: 1px solid;
  border-radius: 20%;
  margin-top: 20px;
}
</style>
