<template>
  <div style="padding-bottom: 35px;">
    <v-row align="center" justify="center">
      <v-col class="text-center" cols="12">
        <h1 class="display-2 font-weight-thin mb-4">{{'Contact'}}</h1>
      </v-col>
    </v-row>
    <v-item-group>
      <v-container>
        <v-row>
          <v-col v-for="account in accounts" :key="account.title" cols="12" sm="4">
            <v-item>
              <div class="text-caption">
                <v-icon large>{{account.icon}}</v-icon>
                {{account.title}}
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
      accounts: [
        {
          icon: "mdi-linkedin",
          title: "Rangie Laurente"
        },
        {
          icon: "mdi-skype",
          title: "Rangie Laurente"
        },
        {
          icon: "mdi-gmail",
          title: "rangie.laurente@student.passerellesnumeriques.org"
        }
      ]
    };
  }
};
</script>

<style>
</style>
