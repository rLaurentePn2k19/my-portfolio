<template>
  <div>
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="display-2 font-weight-thin mb-4">{{'What I do'}}</h1>
      </v-col>
    </v-row>
    <div>
      <div class="text-center">
        <v-row class="mb-6">
          <v-col v-for="skill in skills" :key="skill.title" cols="6" sm="2">
            <v-chip large class="ma-2" :color="skill.color" outlined>
              <span left class="iconify" :data-icon="skill.icon" data-inline="false" data-width="30px"></span>
              <!-- <v-icon left>{{skill.icon}}</v-icon> -->
              {{skill.title}}
            </v-chip>
          </v-col>
        </v-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        {
          icon: "logos:vue",
          title: "HTML",
          color: "#E44D26"
        },
        {
          icon: "whh:cssthree",
          title: "CSS",
          color: "#264de4"
        },
        {
          icon: "logos:javascript",
          title: "JavaScript",
          color: "#F0DB4F"
        },
        {
          icon: "mdi-fan",
          title: "VueJs",
          color: "#41B883"
        },
        {
          icon: "mdi-fan",
          title: "Angular",
          color: "#B52E31"
        },
        {
          icon: "mdi-fan",
          title: "Bootstrap",
          color: "#080135"
        },
        {
          icon: "mdi-vuetify",
          title: "Vuetify",
          color: "indigo"
        },
        {
          icon: "mdi-fan",
          title: "Java",
          color: "#f89820"
        },
        {
          icon: "mdi-fan",
          title: "Python",
          color: "#4B8BBE"
        },
        {
          icon: "mdi-fan",
          title: "NodeJs",
          color: "#68A063"
        },
        {
          icon: "mdi-fan",
          title: "MongoDb",
          color: "#4DB33D"
        },
        {
          icon: "mdi-fan",
          title: "ExpressJs",
          color: "#3C873A"
        }
      ],
      items: [
        {
          src: require("@/assets/logo.png")
        },
        {
          src: require("@/assets/java.png")
        },
        {
          src: require("@/assets/python.png")
        },
        {
          src: require("@/assets/angular.png")
        },
        {
          src: require("@/assets/bootstrap.png")
        },
        {
          src: require("@/assets/js1.png")
        },
        {
          src: require("@/assets/css.png")
        },
        {
          src: require("@/assets/html.png")
        }
      ]
    };
  }
};
</script>

<style>
</style>
