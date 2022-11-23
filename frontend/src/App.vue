<template>
  <v-app>
    <MainHeader/>
    <HomePage/>
    <MainFooter/>
  </v-app>
</template>

<script>
import HomePage from "@/components/HomePage";
import MainHeader from "@/components/MainHeader";
import MainFooter from "@/components/MainFooter";

export default {
  name: 'App',

  components: {
    MainFooter,
    MainHeader,
    HomePage,
  },

  data: () => ({
    //
  }),
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700;800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@400;700;800&display=swap');
#app {
  font-family: 'Oswald', 'Nanum Gothic', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
html,
body {
  background: #faedf0;
}
</style>