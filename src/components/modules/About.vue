<template>
    <v-lazy
        v-model="isActive"
        :options="{
            threshold: 0.5,
        }"
        min-height="200"
        transition="scale-transition"
    >
        <div id="about">
            <div style="padding: 2%">
                <v-row align="center" justify="center">
                    <v-col class="text-center" cols="12">
                        <h1 class="display-2 font-weight-thin mb-4">
                            {{ 'About Me' }}
                        </h1>
                    </v-col>
                </v-row>
                <br />
                <v-timeline align-top :dense="$vuetify.breakpoint.smAndDown">
                    <v-timeline-item
                        v-for="(item, i) in items"
                        :key="i"
                        :color="item.color"
                        fill-dot
                    >
                        <template v-slot:icon>
                            <v-avatar size="60">
                                <img alt="org" :src="item.src" />
                            </v-avatar>
                        </template>
                        <v-hover v-slot="{ hover }">
                            <v-card
                                :color="hover ? item.color : item.color"
                                dark
                                :elevation="hover ? 16 : 2"
                                :class="{ 'on-hover': hover }"
                                min-height="150"
                            >
                                <v-card-title class="title font-weight-light">{{
                                    item.title
                                }}</v-card-title>
                                <v-divider></v-divider>
                                <v-card-text>
                                    {{ item.description }}
                                </v-card-text>
                            </v-card>
                        </v-hover>
                    </v-timeline-item>
                </v-timeline>
            </div>
        </div>
    </v-lazy>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            isActiveItem: false,
            items: [
                {
                    color: '#e4702d',
                    title: 'Me',
                    icon: 'mdi-account',
                    src: require('@/assets/updated-headshot.jpg'),
                    description:
                        'I am passionate about programming and I am always striving hard to learn new technology to create innovative projects. Full-stack Developer is what really I dream to become.'
                },
                {
                    color: '#e4702d',
                    title: 'Organization',
                    icon: ' mdi-account-multiple',
                    src: require('@/assets/pn-logo.png'),
                    description:
                        'I am a scholar of Passerelles numeriques Philippines, a French Non-Government Organization. As scholars, we are trained to become young professionals in the field of Technology, specially in Software Development. '
                },
                {
                    color: '#e4702d',
                    title: 'Education',
                    icon: 'mdi-school',
                    src: require('@/assets/usc.jpg'),
                    description:
                        'I studied at the University of San Carlos-Talamban Campus for 2.5 years with the course of Certificate in Computer Technology (CCT), specialized in Software Development.'
                },
                {
                    color: '#e4702d',
                    title: 'Increment Technologies',
                    icon: 'mdi-school',
                    src: require('@/assets/increment.png'),
                    description: `I was a volunteered Web Developer for 2 months, it was started last July - August 2020, and it helped me to enhanced my skills and knowledge about Web Development. At the same time
          I give my service to the community because the Web Applcation we created was for COVID-19, it is named Birds-eye.org, this Web Application is mainly used for Contact Tracing.`
                },
                {
                    color: '#e4702d',
                    title: 'Softype Philippines Inc.',
                    icon: 'mdi-school',
                    src: require('@/assets/softype.png'),
                    description: `I spent my internship in Softype Philippines Inc. as an Oracle Technical Consultant/Back-End Developer started August - November 2020, and being absorbed as a full-time employee December 2020 - April 2021.`
                },
                {
                    color: '#e4702d',
                    title: 'CrewBloom Inc.',
                    icon: 'mdi-school',
                    src: require('@/assets/crewbloom.png'),
                    description: `Currently working as a Full-Time Junior Web Developer in CrewBloom Inc.`
                }
            ]
        }
    }
}
</script>

<style lang="sass" scoped>
.v-card.on-hover.theme--dark
    background-color: rgba(#FFF, 0.8)
>.v-card__text
    color: #000
</style>