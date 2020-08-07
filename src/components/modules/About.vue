<template>
  <div style="padding: 2%;">
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="display-2 font-weight-thin mb-4">{{'About Me'}}</h1>
      </v-col>
    </v-row>
    <br>
    <v-timeline align-top :dense="$vuetify.breakpoint.smAndDown">
      <v-timeline-item v-for="(item, i) in items" :key="i" :color="item.color" fill-dot>
        <template v-slot:icon>
          <v-avatar size="60">
            <img :src="item.src">
          </v-avatar>
        </template>
        <v-card :color="item.color" dark>
          <v-card-title class="title">{{item.title }}</v-card-title>
          <v-card-text class="white text--primary">
            <p>Gwapo kaayo ko Gwapo kaayo ko Gwapo kaayo ko Gwapo kaayo ko Gwapo kaayo ko Gwapo kaayo ko Gwapo kaayo ko</p>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          color: "#C62828",
          title: "Me",
          icon: "mdi-account",
          src: require("@/assets/me1.jpg"),
          description: ""
        },
        {
          color: "#FB8C00",
          title: "Organization",
          icon: " mdi-account-multiple",
          src: require("@/assets/pn-logo.png")
        },
        {
          color: "#43A047",
          title: "Education",
          icon: "mdi-school",
          src: require("@/assets/usc.jpg")
        }
      ],
      description:
        "I am an energetic, ambitious person who has developed a mature and responsible approach to any task that I undertake, or situation that I am presented with. As a graduate with three years’ experience in management, I am excellent in working with others to achieve a certain objective on time and with excellence. In my previous role, I improved the performance, operations and productivity of my team by 35%."
    };
  }
};
</script>

<style>
</style>
