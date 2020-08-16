<template>
  <div id="home">
    <v-parallax dark :src="require('@/assets/test2.jpg')" height="700">
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-2 font-weight-thin mb-4">{{name}}</h1>
          <h4 class="display-1 font-weight-thin mb-4">{{position}}</h4>
          <v-btn
            class="ma-2"
            href="./resume/Rangie.Laurente.Resume.pdf"
            small
            outlined
            color="#EF5350"
          >View resume</v-btn>
          <a>
            <v-btn class="ma-2" target="_blank" small outlined color="#EF5350" href="https://github.com/rLaurentePn2k19"><v-icon>mdi-github</v-icon>View Github</v-btn>
          </a>
        </v-col>
      </v-row>
    </v-parallax>
  </div>
</template>

<script>
export default {
  name: "Parallax",
  data() {
    return {
      name: "Hi, I'm Rangie Laurente,",
      position: "I am a Web Developer."
    };
  }
};
</script>

<style lang="sass">

$parallax-perspective : 1 !default
$parallax-element     : "body" !default
$parallax-ios         : true !default

</style>
