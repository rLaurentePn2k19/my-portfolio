<template>
  <div>
    <Parallax/>
    <br>
    <About/>
    <br>
    <Skills/>
    <br>
    <Projects/>
    <br>
    <Contact/>
  </div>
</template>

<script>
import Parallax from "../Parallax.vue";
import About from "../About.vue";
import Skills from "../Skills.vue";
import Contact from "../Contact.vue";
import Projects from "../Projects.vue";

export default {
  components: {
    Parallax,
    About,
    Contact,
    Skills,
    Projects
  }
};
</script>

<style>
</style>
