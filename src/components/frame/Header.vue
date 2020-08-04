<template>
  <div>
    <v-app-bar app color="#F5F5F5" inverted-scroll>
      <!-- <v-app-bar app color="#1d1f20" color="white" dark elevate-on-scroll> -->
      <v-spacer></v-spacer>
      <div class="d-flex align-center">
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn target="_blank" text v-bind="attrs" v-on="on">
              <span class="shrink mt-1 hidden-sm-and-down">Home</span>
              <v-icon>mdi-home</v-icon>
            </v-btn>
          </template>
          <span>Home</span>
        </v-tooltip>
        <v-btn target="_blank" text>
          <span class="shrink mt-1 hidden-sm-and-down">Skills</span>
          <v-icon>mdi-code-tags</v-icon>
        </v-btn>
        <v-avatar>
          <img
            class="shrink mr-1"
            id="loading"
            transition="scale-transition"
            :src="require('@/assets/code2.png')"
          >
        </v-avatar>
        <v-btn target="_blank" text>
          <span class="shrink mt-1 hidden-sm-and-down">About</span>
          <v-icon>mdi-account</v-icon>
        </v-btn>
        <v-btn target="_blank" text>
          <span class="shrink mt-1 hidden-sm-and-down">Contact</span>
          <v-icon>mdi-phone</v-icon>
        </v-btn>
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

