<template>
  <v-app id="app">
    <v-main>
      <Header></Header>
      <Home></Home>
    </v-main>
  </v-app>
</template>

<script>
import Header from "@/components/frame/Header.vue";
import Home from "@/components/modules/Landing/Home.vue";

export default {
  data() {
    return {};
  },
  components: {
    Header,
    Home
  }
};
</script>

<style>
#app {
  /* height: 200vh; */
  background-color: #F5F5F5;
}
</style>
