<template>
    <v-lazy
        v-model="isActive"
        :options="{
            threshold: 0.5,
        }"
        min-height="200"
        transition="scale-transition"
    >
        <div id="contact">
            <div style="padding-bottom: 35px">
                <v-row align="center" justify="center">
                    <v-col class="text-center" cols="12">
                        <h1 class="display-2 font-weight-thin mb-4">
                            {{ 'Contact' }}
                        </h1>
                    </v-col>
                </v-row>
                <v-item-group>
                    <v-container>
                        <v-row>
                            <v-col
                                :class="
                                    $vuetify.breakpoint.smAndDown
                                        ? 'd-flex justify-start'
                                        : 'd-flex justify-center'
                                "
                                v-for="account in accounts"
                                :key="account.icon"
                                cols="12"
                                sm="4"
                            >
                                <v-item>
                                    <div class="text-caption">
                                        <v-icon large>{{
                                            account.icon
                                        }}</v-icon>
                                        {{ account.title }}
                                    </div>
                                </v-item>
                            </v-col>
                        </v-row>
                    </v-container>
                </v-item-group>
            </div>
        </div>
    </v-lazy>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            accounts: [
                {
                    icon: 'mdi-linkedin',
                    title:
                        'https://www.linkedin.com/in/rangie-laurente-486600195/'
                },
                {
                    icon: 'mdi-skype',
                    title: 'live:.cid.f71411395c2ea3a6'
                },
                {
                    icon: 'mdi-gmail',
                    title: 'rangielaurente12stem@gmail.com'
                }
            ]
        }
    }
}
</script>
