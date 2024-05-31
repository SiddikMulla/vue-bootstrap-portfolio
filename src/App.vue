<template>
  <img class="img-fluid" style="width: 100px; height: 70px" alt="Vue logo" src="./assets/image.png" />
  <AppHeader />
  <router-view />
  <!-- <AppFooter /> -->

</template>

<script>
import AppHeader from "./components/Header.vue";
// import AppFooter from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    // AppFooter,
  },
};
</script>

<style>
#app {
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  font-family: "Merriweather Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  /* margin-top: 60px; */
  background-color: #cccccc;
  background-image: url("./assets/bg.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>
