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
          <v-col v-for="project in projects" :key="project.title" cols="12" md="4">
            <v-item>
              <div class="text-caption">
                <v-card class="mx-auto" max-width="344">
                  <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" height="200px"></v-img>

                  <v-card-title>{{project.title}}</v-card-title>

                  <v-card-subtitle>Description: </v-card-subtitle>
                  <v-card-actions>
                    <v-btn text fab small>
                      <v-icon>mdi-github</v-icon>
                    </v-btn>
                    <v-spacer></v-spacer>
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
          title: "Abangbalay"
        },
        {
          title: "OnlinePharmacy"
        },
        {
          title: "SoftypeFoodOrder"
        }
      ]
    };
  }
};
</script>

<style>
</style>
