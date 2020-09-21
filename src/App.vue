<template>
  <div id="app">
    <Header></Header>
    <router-view></router-view>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import HomePage from "./HomePage.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    HomePage,
    Footer
  }
};
</script>

<style>
:root {
  --first-color: #e67e22; //11
  --third-color: #747474;
  --second-color: #3a392b;
  --font-family: "Poppins", sans-serif;
}
</style>
