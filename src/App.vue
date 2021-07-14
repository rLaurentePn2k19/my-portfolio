<template>
    <v-app id="app">
        <Header></Header>
        <v-main>
            <Main></Main>
        </v-main>
    </v-app>
</template>

<script>
import Header from '@/components/frame/Header.vue'
import Main from '@/components/modules/Landing/Main.vue'

export default {
    data() {
        return {}
    },
    components: {
        Header,
        Main
    }
}
</script>

<style>
#app {
    background-color: #f5f5f5;
}
</style>
