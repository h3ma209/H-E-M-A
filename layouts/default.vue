<template>
    <v-app fluid>

        <v-app-bar :clipped-left="clipped" fixed flat app style="background:#ffffff">
            <v-spacer></v-spacer>
            <v-toolbar-title v-text="title" />
            <v-spacer />
            <v-toolbar-items class="ma-14">
                <v-btn v-bind:class="{ 'font-weight-bold': item.active }" color="navbartext" text v-for="item in items" :key="item.icon" :href="item.to" target="_blank" :title="item.title" style="color:white;">{{ item.title }}</v-btn>
            </v-toolbar-items>
            <v-spacer></v-spacer>
        </v-app-bar>

        <v-main style="position:relative;height:100;">
            <v-container class="fill-height fill-height ma-0 pa-0" fluid>
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
                    title: 'My CV',
                    to: 'https://drive.google.com/file/d/1bhpjJcbszj6sj58JtR_bkTHJD-5HF7Yp/view?usp=sharing'
                },
                {
                    title: 'Portfolio',
                    to:'https://drive.google.com/file/d/14WyCpHtfpTxASUZq0-SiKzx-y9qw1-N5/view?usp=sharing'
                },
                {
                    title: 'Contact Me',
                    to:'mailto:hema.omer007@gmail.com'
                },
            ],

            right: true,
            title: 'H E M A .'
        }
    }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&display=swap");
@import url("https://use.fontawesome.com/releases/v5.0.13/css/all.css");
html,
body {
    margin: 0;
    padding: 0;
}
.v-application {
    font-family: "Montserrat", sans-serif;
    padding: 0;
    margin: 0;
}
</style>
