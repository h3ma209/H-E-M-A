<template>
    <v-app fluid>

        <v-app-bar :clipped-left="clipped" fixed flat app style="background:#ffffff">
            <v-spacer></v-spacer>
            <v-toolbar-title v-text="title" />
            <v-spacer />
            <v-toolbar-items class="ma-14">
                <v-btn v-bind:class="{ 'font-weight-bold': item.active }" color="navbartext" text v-for="item in items" :key="item.icon" to="#" :title="item.title" style="color:white;">{{ item.title }}</v-btn>
            </v-toolbar-items>
            <v-spacer></v-spacer>
        </v-app-bar>

        <v-main  style="position:relative;height:100">
            <v-container class="fill-height" fluid>
                <nuxt />
            </v-container>
        </v-main>

        <v-footer :absolute="!fixed" app>
            <span>&copy; {{ new Date().getFullYear() }}</span>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    
    data() {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            items: [
                {
                    icon: 'mdi-apps',
                    title: 'Home',
                    to: '/',
                    active: true,
                },
                {
                    icon: 'mdi-chart-bubble',
                    title: 'About Me',
                    to: '/inspire'
                },
                {
                    title: 'Contact Me'
                },
                {
                    title: 'Portfolio'
                }
            ],

            right: true,
            title: 'H E M A .'
        }
    }
}
</script>

<style scoped>
.v-application{
  font-family: 'Montserrat', sans-serif;
  padding: 0;
  margin: 0;
}
</style>
