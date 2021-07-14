<template>
    <v-lazy
        v-model="isActive"
        :options="{
            threshold: 0.5,
        }"
        min-height="200"
        transition="scale-transition"
    >
        <div id="skills">
            <v-row align="center" justify="center">
                <v-col class="text-center" cols="12">
                    <h1 class="display-2 font-weight-thin mb-4">
                        {{ 'What I do' }}
                    </h1>
                </v-col>
            </v-row>
            <v-row class="mb-6">
                <v-col
                    v-for="skill in skills"
                    :key="skill.title"
                    cols="12"
                    md="3"
                    sm="6"
                    class="d-flex justify-center"
                >
                    <v-hover v-slot="{ hover }">
                        <v-chip
                            large
                            class="ma-2 short"
                            :color="hover ? skill.color : ''"
                            outlined
                        >
                            <iconify-icon
                                class="mx-1"
                                :data-icon="skill.icon"
                                data-width="30px"
                            ></iconify-icon>
                            <span>
                                {{ skill.title }}
                            </span>
                        </v-chip>
                    </v-hover>
                </v-col>
            </v-row>
        </div>
    </v-lazy>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            skills: [
                {
                    icon: 'mdi:language-html5',
                    title: 'HTML',
                    color: '#E44D26'
                },
                {
                    icon: 'ion:logo-css3',
                    title: 'CSS',
                    color: '#264de4'
                },
                {
                    icon: 'logos:javascript',
                    title: 'JavaScript',
                    color: '#F0DB4F'
                },
                {
                    icon: 'logos:vue',
                    title: 'VueJs',
                    color: '#41B883'
                },
                {
                    icon: 'mdi:angular',
                    title: 'Angular',
                    color: '#B52E31'
                },
                {
                    icon: 'mdi:bootstrap',
                    title: 'Bootstrap',
                    color: '#080135'
                },
                {
                    icon: 'mdi-vuetify',
                    title: 'Vuetify',
                    color: 'indigo'
                },
                {
                    icon: 'logos:nodejs',
                    title: 'NodeJs',
                    color: '#68A063'
                },
                {
                    icon: 'mdi:react',
                    title: 'ReactJs',
                    color: '#61dafb'
                },
                {
                    icon: 'mdi:laravel',
                    title: 'PHP Laravel',
                    color: '#fb503b'
                },
                {
                    icon: 'vscode-icons:file-type-mysql',
                    title: 'MySQL',
                    color: '#00758F'
                },
                {
                    icon: 'cib:oracle-netsuite',
                    title: 'Oracle NetSuite',
                    color: '#000000'
                },
                {
                    icon: 'mdi-rocket-launch-outline',
                    title: 'Strapi',
                    color: '#8a71f8'
                },
                {
                    icon: 'mdi-nuxt',
                    title: 'NuxtJs',
                    color: '#55b983'
                }
            ]
        }
    }
}
</script>

<style scoped>
.short {
    width: 150px;
}
</style>
