<template>
  <div>
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
                    <v-btn fab small text>
                      <v-icon>{{project.repo}}</v-icon>
                    </v-btn>
                    <iconify-icon
                      :data-icon="project.deploy"
                      data-width="20"
                      style="cursor: pointer"
                    ></iconify-icon>
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
          repo: "mdi-github"
        },
        {
          title: "Pharmacy",
          description:
            "A Web application which provides a list of cheap boarding houses where the user can ",
          technology_used: ["logos:java"],
          repo: "mdi-github"
        },
        {
          title: "SoftypeFoodOrder",
          description:
            "A Web application which provides a list of cheap boarding houses where the user can ",
          technology_used: [
            "logos:vuetifyjs",
            "logos:vue",
            "logos:nodejs",
            "logos:nodejs-icon",
            "cib:mongodb"
          ],
          repo: "mdi-github",
          deploy: "logos:netlify"
        },
        {
          title: "MQTT Web Socket",
          description:
            "A Web application which provides a list of cheap boarding houses where the user can ",
          technology_used: [
            "logos:html-5",
            "logos:css-3",
            "cib:jquery",
            "logos:bootstrap",
            "gg:bee"
          ],
          repo: "mdi-github",
          deploy: "logos:github-octocat"
        },
        {
          title: "Socket.io Chat app",
          description:
            "A Web application which provides a list of cheap boarding houses where the user can ",
          technology_used: [
            "logos:html-5",
            "logos:css-3",
            "cib:jquery",
            "logos:bootstrap",
            "cib:socket-io"
          ],
          repo: "mdi-github",
          deploy: "logos:heroku-icon"
        }
      ]
    };
  }
};
</script>

<style>
</style>
