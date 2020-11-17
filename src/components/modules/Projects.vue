<template>
  <div id="projects">
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="display-2 font-weight-thin mb-4">{{'Projects'}}</h1>
      </v-col>
    </v-row>
    <v-item-group>
      <v-container>
        <v-row>
          <v-col v-for="project in projects" :key="project.title" cols="12" sm="4">
            <v-item>
              <div class="text-caption">
                <v-card color="#424242" dark>
                  <v-card-title class="title">{{project.title }}</v-card-title>
                  <v-card-text class="white text--primary">
                    <br>
                    <p>
                      <strong>Description:</strong>
                      {{project.description}}
                    </p>
                    <div>
                      <strong>Technology used:</strong>
                      <iconify-icon
                        v-for="icon in project.technology_used"
                        :key="icon"
                        :data-icon="icon"
                        data-width="20"
                      ></iconify-icon>
                    </div>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn
                      :href="rep.link"
                      fab
                      small
                      text
                      v-for="rep in project.repo"
                      :key="rep.icon"
                    >
                      <v-icon>{{rep.icon}}</v-icon>
                    </v-btn>
                    Github
                  </v-card-actions>
                </v-card>
              </div>
            </v-item>
          </v-col>
        </v-row>
      </v-container>
    </v-item-group>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Abangbalay",
          description:
            "A Web application which provides a list of cheap boarding houses where the user can ",
          technology_used: [
            "logos:vuetifyjs",
            "logos:vue",
            "logos:nodejs",
            "logos:nodejs-icon",
            "cib:mongodb"
          ],
          repo: [
            {
              icon: "mdi-github",
              link: "https://github.com/rLaurentePn2k19/abangbalay"
            }
          ]
        },
        {
          title: "SoftypeFoodOrder",
          description: "It is a web application for food ordering system.",
          technology_used: [
            "logos:vuetifyjs",
            "logos:vue",
            "logos:nodejs",
            "logos:nodejs-icon",
            "cib:mongodb"
          ],
          repo: [
            {
              icon: "mdi-github",
              link: "https://github.com/rLaurentePn2k19/sfosfe"
            }
          ]
        },
        {
          title: "MQTT Web Socket",
          description:
            "A web application where you can publish and subscribe a topic through MQTT.",
          technology_used: [
            "logos:html-5",
            "logos:css-3",
            "cib:jquery",
            "logos:bootstrap",
            "gg:bee"
          ],
          repo: [
            {
              icon: "mdi-github",
              link:
                "https://github.com/rLaurentePn2k19/rLaurentePn2k19.github.io"
            }
          ]
        },
        {
          title: "Softype Employee Portal",
          description:
            "It is a Web Application for HRMS, it caters leave requests, office requests, company repository, organizational chart and employee directory which can make the access of all the employee centralized.",
          technology_used: [
            "mdi:react",
            "mdi:laravel",
            "vscode-icons:file-type-mysql"
          ],
          repo: [
            {
              icon: "mdi-github",
              link: "https://github.com/rLaurentePn2k19/OnlinePharmacy"
            }
          ]
        }
      ]
    };
  }
};
</script>

<style>
</style>
