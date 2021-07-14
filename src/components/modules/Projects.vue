<template>
    <v-lazy
        v-model="isActive"
        :options="{
            threshold: 0.5,
        }"
        min-height="200"
        transition="scale-transition"
    >
        <v-parallax
            dark
            :src="require('@/assets/layered-peaks-haikei.svg')"
            :height="parallaxHeight"
        >
            <div id="projects">
                <v-row align="center" justify="center">
                    <v-col class="text-center" cols="12">
                        <h1 class="display-2 font-weight-thin mb-4">
                            {{ 'Projects' }}
                        </h1>
                    </v-col>
                </v-row>
                <v-item-group>
                    <v-container>
                        <v-row>
                            <v-col
                                cols="12"
                                md="3"
                                v-for="(project, i) in projects"
                                :key="i"
                            >
                                <v-item v-slot="{ active, toggle }">
                                    <v-card
                                        :color="active ? '#e4702d' : '#f5f5f5'"
                                        flat
                                        height="250"
                                        class="card-title"
                                        @click="toggle"
                                    >
                                        <div
                                            v-if="!active"
                                            class="title font-weight-thin"
                                        >
                                            {{ project.title }}
                                        </div>
                                        <div
                                            v-else
                                            class="
                                                subtitle-1
                                                white--text
                                                font-weight-light
                                                text-center
                                                px-4
                                            "
                                        >
                                            {{ project.description }}
                                        </div>
                                    </v-card>
                                </v-item>
                            </v-col>
                        </v-row>
                    </v-container>
                </v-item-group>
            </div>
        </v-parallax>
    </v-lazy>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            projects: [
                {
                    title: 'Abangbalay',
                    description:
                        'A Web Application which provides a list of cheap boarding houses where the user can ',
                    technology_used: [
                        'logos:vuetifyjs',
                        'logos:vue',
                        'logos:nodejs',
                        'logos:nodejs-icon',
                        'cib:mongodb'
                    ],
                    repo: [
                        {
                            icon: 'mdi-github',
                            link:
                                'https://github.com/rLaurentePn2k19/abangbalay'
                        }
                    ]
                },
                {
                    title: 'SoftypeFoodOrder',
                    description:
                        'It is a Web Application for food ordering system, which I made during my Internship.',
                    technology_used: [
                        'logos:vuetifyjs',
                        'logos:vue',
                        'logos:nodejs',
                        'logos:nodejs-icon',
                        'cib:mongodb'
                    ],
                    repo: [
                        {
                            icon: 'mdi-github',
                            link: 'https://github.com/rLaurentePn2k19/sfosfe'
                        }
                    ]
                },
                {
                    title: 'MQTT Web Socket',
                    description:
                        'A Web Application where you can publish and subscribe a topic through MQTT.',
                    technology_used: [
                        'logos:html-5',
                        'logos:css-3',
                        'cib:jquery',
                        'logos:bootstrap',
                        'gg:bee'
                    ],
                    repo: [
                        {
                            icon: 'mdi-github',
                            link:
                                'https://github.com/rLaurentePn2k19/rLaurentePn2k19.github.io'
                        }
                    ]
                },
                {
                    title: 'Softype Employee Portal',
                    description:
                        'It is a Web Application for HRMS, it caters leave requests, office requests, company repository, organizational chart and employee directory which can make the access of all the employee centralized.',
                    technology_used: [
                        'mdi:react',
                        'mdi:laravel',
                        'vscode-icons:file-type-mysql'
                    ],
                    repo: [
                        {
                            icon: 'mdi-github',
                            link:
                                'https://github.com/rLaurentePn2k19/OnlinePharmacy'
                        }
                    ]
                }
            ]
        }
    },

    computed: {
        parallaxHeight() {
            if (this.$vuetify.breakpoint.smAndDown) {
                return '100%'
            }
            return '600'
        }
    }
}
</script>

<style scoped>
.card-title {
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>