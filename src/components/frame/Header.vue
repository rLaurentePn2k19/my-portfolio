<template>
  <div>
    <v-app-bar app color="#F5F5F5" inverted-scroll>
      <!-- <v-app-bar app color="#1d1f20" color="white" dark elevate-on-scroll> -->
      <v-spacer></v-spacer>
      <div class="d-flex align-center">
        <a href="#home">
          <v-btn target="_blank" text>
            <span class="shrink mt-1 hidden-sm-and-down">Home</span>
            <v-icon>mdi-home</v-icon>
          </v-btn>
        </a>
        <a href="#skills" >
          <v-btn target="_blank" text >
            <span class="shrink mt-1 hidden-sm-and-down" >Skills</span>
            <v-icon>mdi-code-tags</v-icon>
          </v-btn>
        </a>
        <v-avatar>
          <img
            class="shrink mr-1"
            id="loading"
            transition="scale-transition"
            :src="require('@/assets/code2.png')"
          >
        </v-avatar>
        <a href="#about">
          <v-btn target="_blank" text>
            <span class="shrink mt-1 hidden-sm-and-down">About</span>
            <v-icon>mdi-account</v-icon>
          </v-btn>
        </a>
        <a href="#contact">
          <v-btn target="_blank" text>
            <span class="shrink mt-1 hidden-sm-and-down">Contact</span>
            <v-icon>mdi-phone</v-icon>
          </v-btn>
        </a>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>
  </div>
</template>



<style>
#loading {
  -webkit-animation: rotation 2s infinite linear;
}

@-webkit-keyframes rotation {
  from {
    -webkit-transform: rotate(0deg);
  }
  to {
    -webkit-transform: rotate(359deg);
  }
}

a {
  text-decoration: none;
}
</style>


<script>
export default {
  data: () => ({
    isMobile: false
    // :src="require('../assets/fireball.png')"
  }),

  beforeDestroy() {
    if (typeof window !== "undefined") {
      window.removeEventListener("resize", this.onResize, { passive: true });
    }
  },

  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },

  methods: {
    onResize() {
      this.isMobile = window.innerWidth < 600;
    }
  }
};
</script>

