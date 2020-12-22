<template>
  <div id="about">
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
              <br>
              <p>{{item.description}}</p>
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          color: "#EF5350",
          title: "Me",
          icon: "mdi-account",
          src: require("@/assets/me1.jpg"),
          description:
            "I am passionate about programming and I am always striving hard to learn new technology to create innovative projects. Full-stack Developer is what really I dream to become."
        },
        {
          color: "#4B8BBE",
          title: "Organization",
          icon: " mdi-account-multiple",
          src: require("@/assets/pn-logo.png"),
          description:
            "I am a scholar of Passerelles numeriques Philippines, a French Non-Government Organization. As scholars, we are trained to become young professionals in the field of Technology, specially in Software Development."
        },
        {
          color: "#43A047",
          title: "Education",
          icon: "mdi-school",
          src: require("@/assets/usc.jpg"),
          description:
            "I am currently studying at the University of San Carlos-Talamban Campus for 2.5 years with the course of Certificate in Computer Technology (CCT), specialized in Software Development."
        },
        {
          color: "#212529",
          title: "Increment Technologies",
          icon: "mdi-school",
          src: require("@/assets/increment.png"),
          description:
            `I was a volunteered Web Developer for 2 months and it helped me to enhanced my skills and knowledge about web development.` 
        },
        {
          color: "#E4691C",
          title: "Softype Philippines Inc.",
          icon: "mdi-school",
          src: require("@/assets/softype.png"),
          description:
            "I am an Intern Technical Consultant, I do solving technical problems whenever client facing techical issues. (August 2020 - Present)"
        }
      ]
    };
  }
};
</script>

<style>
</style>
