<template>
    <div>
        <v-app-bar app color="#F5F5F5" inverted-scroll>
            <v-spacer></v-spacer>
            <div class="d-flex align-center">
                <a href="#home">
                    <v-btn target="_blank" text>
                        <v-icon left>mdi-home</v-icon>
                        <span class="shrink mt-1 hidden-sm-and-down">Home</span>
                    </v-btn>
                </a>
                <a href="#skills">
                    <v-btn target="_blank" text>
                        <v-icon left>mdi-code-tags</v-icon>
                        <span class="shrink mt-1 hidden-sm-and-down"
                            >Skills</span
                        >
                    </v-btn>
                </a>
                <v-avatar>
                    <img
                        alt="logo"
                        class="shrink mr-1"
                        id="loading"
                        transition="scale-transition"
                        :src="require('@/assets/code2.png')"
                    />
                </v-avatar>
                <a href="#about">
                    <v-btn target="_blank" text>
                        <v-icon left>mdi-account</v-icon>
                        <span class="shrink mt-1 hidden-sm-and-down"
                            >About</span
                        >
                    </v-btn>
                </a>
                <a href="#projects">
                    <v-btn target="_blank" text>
                        <v-icon left>mdi-view-list</v-icon>
                        <span class="shrink mt-1 hidden-sm-and-down"
                            >Projects</span
                        >
                    </v-btn>
                </a>
            </div>

            <v-spacer></v-spacer>
        </v-app-bar>
    </div>
</template>

<script>
export default {
    data: () => ({
        isMobile: false
        // :src="require('../assets/fireball.png')"
    }),

    beforeDestroy() {
        if (typeof window !== 'undefined') {
            window.removeEventListener('resize', this.onResize, {
                passive: true
            })
        }
    },

    mounted() {
        this.onResize()
        window.addEventListener('resize', this.onResize, { passive: true })
    },

    methods: {
        onResize() {
            this.isMobile = window.innerWidth < 600
        }
    }
}
</script>

<style>
#loading {
    -webkit-animation: rotation 2s infinite linear;
}

@-webkit-keyframes rotation {
    from {
        -webkit-transform: rotate(0deg);
    }
    to {
        -webkit-transform: rotate(359deg);
    }
}

a {
    text-decoration: none;
}
</style>