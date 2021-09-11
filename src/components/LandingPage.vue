<template>
  <div class="hello">
    <div class="items clickable">
      <div>
        &lt;<input class="placeholder"
          v-model="placeholder"
          placeholder="education,social &#38; skills"
          type="text"
          maxlength="18"
        />
      </div>
    </div>
    <div class="items interactive">
      <div class="enter">&lt; {{ placeholder }} /&gt;</div>
    </div>
  </div>
</template>

<script>
import { gsap } from "gsap";

export default {
  name: "LandingPage",
  data() {
    return {
      placeholder: "",
    };
  },
  mounted: function () {
    const tl = gsap.timeline({ paused: true });
    document.querySelector(".enter").addEventListener("click", () => {
      tl.resume();
    });
    tl.to(".interactive", {
      duration: 0.5,
      color: "rgb(243, 4, 252)",
      ease: "power1.out",
      width: "60%",
      height: "100px",
    })
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech&display=swap');
.hello {
  display: grid;
  place-items: center;
  grid-template-rows: 2fr 3fr;
  border: 2px solid black;
  background: rgba(22, 21, 21, 1);
  width: 70%;
  justify-content: center;
  text-align: center;
  margin: auto;
  border-radius: 10px;
}
.items {
  place-self: center;
}
h1 {
  color: rgb(206, 29, 197);
}
.enter {
  border: 1px solid whitesmoke;
  border-radius: 2px;
  padding: 5px;
}
.interactive {
  margin: 30px;
  color: rgb(206, 29, 197);
  border: 2px solid rgb(206, 29, 197);
  padding: 5%;
}
.placeholder{
    background: black;
    border-radius: 5px;
    color: rgb(206, 29, 197);
    padding: 10px;
    border: none;
    text-align: center;
    font-family: 'Share Tech', sans-serif;

}
.placeholder:focus{
    border-bottom: 3px solid rgb(206, 29, 197);
    border-left: 3px solid rgb(206, 29, 197);
    outline: none;
}
</style>
