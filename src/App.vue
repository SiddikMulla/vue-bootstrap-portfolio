<template>
  <div class="image-container">
    <img class="img-fluid" style="width: 100px; height: 70px" alt="Vue logo" src="./assets/image.png" />
  </div>
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
  font-family: "Merriweather Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  background-color: #cccccc;
  background: url(https://res.cloudinary.com/ritalbradley/image/upload/v1657644013/pexels-elijah-o_donnell-3473569_o7ohfd.jpg) center/cover no-repeat fixed;

}

.image-container {
  display: inline-block;
  position: relative;
}

.img-fluid {
  width: 100px;
  height: 70px;
  position: relative;
  z-index: 1;
}

.image-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('./assets/image.png') no-repeat center/contain;
  filter: drop-shadow(0px 4px 6px rgba(251, 230, 136, 0.715));
  z-index: 0;
}
</style>
