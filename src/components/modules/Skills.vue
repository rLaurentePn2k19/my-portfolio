<template>
  <div id="skills">
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
              <iconify-icon :data-icon="skill.icon" data-width="30px"></iconify-icon>
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
          icon: "mdi:language-html5",
          title: "HTML",
          color: "#E44D26"
        },
        {
          icon: "ion:logo-css3",
          title: "CSS",
          color: "#264de4"
        },
        {
          icon: "logos:javascript",
          title: "JavaScript",
          color: "#F0DB4F"
        },
        {
          icon: "logos:vue",
          title: "VueJs",
          color: "#41B883"
        },
        {
          icon: "mdi:angular",
          title: "Angular",
          color: "#B52E31"
        },
        {
          icon: "mdi:bootstrap",
          title: "Bootstrap",
          color: "#080135"
        },
        {
          icon: "mdi-vuetify",
          title: "Vuetify",
          color: "indigo"
        },
        {
          icon: "mdi:language-java",
          title: "Java",
          color: "#f89820"
        },
        {
          icon: "mdi:language-python",
          title: "Python",
          color: "#4B8BBE"
        },
        {
          icon: "logos:nodejs",
          title: "NodeJs",
          color: "#68A063"
        },
        {
          icon: "cib:mongodb",
          title: "MongoDb",
          color: "#4DB33D"
        },
        {
          icon: "mdi:nodejs",
          title: "ExpressJs",
          color: "#3C873A"
        },
        {
          icon: "mdi:react",
          title: "ReactJs",
          color: "#61dafb"
        },
        {
          icon: "mdi:laravel",
          title: "PHP Laravel",
          color: "#fb503b"
        },
        {
          icon: "vscode-icons:file-type-mysql",
          title: "MySQL",
          color: "#00758F"
        }
      ]
    };
  }
};
</script>

<style>
</style>
