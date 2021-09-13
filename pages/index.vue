<template>
    <div class="page">
        <v-overlay z-index="999999999" :value="overlay">
            <v-card >
                <v-carousel v-model="model">
                    <v-carousel-item v-for="(ui, i) in uis" :key="i" >
                        <v-img :src="ui.img" contain>

                        </v-img>
                    </v-carousel-item>
                </v-carousel>
            </v-card>
            <v-btn @click="overlay = !overlay">Close</v-btn>
        </v-overlay>
        <div class="landing">
            <v-img src="/white_eclipse.svg" class="eclipse" max-height="150px"></v-img>
            <v-row no-gutter class="text-center mt-14" align="center" justify="center">
                <h1 class="font-weight-regular mt-12">I'm <span class="primary--text font-weight-regular">Hema</span>, Im a Fullstack developer and a UI/UX designer</h1>
            </v-row>
            <v-row class="dots" align="center" justify="center">
                <v-col align="center" justify="center">
                    <v-img src="/dot.svg" max-width="60%" style="opacity:0.7;"></v-img>
                </v-col>
            </v-row>
            <v-row class="landing-content" align="end" justify="center">
                <v-row no-gutters class="skills">

                    <v-col align-self="start" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            Front-end
                        </v-card>
                    </v-col>
                    <v-col align-self="end" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            Back-end
                        </v-card>
                    </v-col>

                    <v-col align-self="center" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            UI/UX
                        </v-card>
                    </v-col>
                </v-row>

                <div class="img">

                    <v-img contain max-height="650" max-width="550" src="/test.png"></v-img>
                </div>
                <div class="purple-blur"></div>
            </v-row>

        </div>
        <div class="social-media">
            <v-row align="center">
                <v-spacer></v-spacer>
                <v-spacer></v-spacer>
                <v-col class="text-center white--text"><i class="fab fa-twitter d-grid"></i></v-col>
                <v-col class="text-center white--text"><i class="fab fa-dribbble-square"></i></v-col>
                <v-col class="text-center white--text"><i class="fab fa-github-square"></i></v-col>
                <v-spacer></v-spacer>
                <v-spacer></v-spacer>
            </v-row>
        </div>
        <div class="about-me">
            <h1>ss</h1>
        </div>
        <div class="ui-portfolio d-flex justify-center align-center mb-6 pa-2">
            <v-row style="background:red" align="center" justify="center">
                <v-col class="pa-1 ma-4 d-flex justify-center align-center" lg='3' xs='1'   style="background:pink" v-for="ui,i in uis" :key="i">
                    <!-- <v-img :src="ui.img" max-height="300"></v-img> -->
                    <v-hover>
                        <template v-slot:default="{ hover }">
                            <v-card class="mx-auto" >
                                <v-img :src="ui.img" max-width="350"></v-img>
                                <v-fade-transition>
                                    <v-overlay v-if="hover" absolute color="#036358">
                                        <v-btn @click="overlay = !overlay">See more info</v-btn>
                                    </v-overlay>
                                </v-fade-transition>

                            </v-card>
                        </template>
                    </v-hover>
                </v-col>
            </v-row>
        </div>
        <div class="projects-portfolio pr-4 pl-4" align='center' justify="space-between">
            <Project v-for="project,i in projects" :key="i" :project="project"></Project>
        </div>
    </div>

</template>

<script>
import Header from "@/components/Typo/Header.vue"
import Project from "@/components/Project.vue"

export default {
    components: {
        Header,
        Project
    },
    data() {
        return {
            model: 0,
            
            projects: [
                { title: 'CRM', tech: 'Bootsrap, PHP, Laravel', description: 'Customer relations project i made for SmartMed.com fully secure and responsive', source: '', live: '', img: 'https://camo.githubusercontent.com/0b89e43464db6e41ca59cb65d8ace2ea5a76f26940a5644ea7c82e7a17abf5b1/68747470733a2f2f63646e2e6472696262626c652e636f6d2f75736572732f353637353133392f73637265656e73686f74732f31353631303431312f6d656469612f33633433633365386131646232316430666234343639626634643731313131312e6a70673f636f6d70726573733d3126726573697a653d38303078363030' },
                { title: 'Ford UI', tech: 'Bootsrap, PHP, Laravel', description: 'Made this for my dream car', source: '', live: '', img: 'https://raw.githubusercontent.com/h3ma209/ui-designs-xd/main/adept/Web%201920%20%E2%80%93%203.png' },
                { title: 'Mustang UI', tech: 'Bootsrap, PHP, Laravel', description: 'Made this for my dream car', source: '', live: '', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527090/media/1a6cf7d0bc3ba48442e948e754e99e2a.jpg?compress=1&resize=800x600' },
            ],
            uis: [
                { title: 'lorem ipsum', link: '', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527004/media/991a173559cb2938f3ccccc242a2095f.jpg?compress=1&resize=800x600' },
                { title: 'lorem ipsum', link: '', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527004/media/991a173559cb2938f3ccccc242a2095f.jpg?compress=1&resize=800x600' },
                { title: 'lorem ipsum', link: '', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527004/media/991a173559cb2938f3ccccc242a2095f.jpg?compress=1&resize=800x600' },
                { title: 'lorem ipsum', link: '', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527004/media/991a173559cb2938f3ccccc242a2095f.jpg?compress=1&resize=800x600' },
            ],
            overlay: false,
        }
    }
}
</script>

<style scoped>
.page {
    height: 100%;
    width: 100%;
    font-family: "Montserrat", sans-serif;
}
.eclipse {
    position: absolute;
    top: 0;
    left: 0;
}

/* Landing */
.landing {
    overflow: hidden !important;
}
.purple-blur {
    background: radial-gradient(#150dfb, #726eec, #ffffff);
    border-radius: 50%;
    opacity: 0.7;
    height: 100%;
    width: 60%;
    filter: blur(700px);
    position: absolute;
    bottom: -200px;
    z-index: 1;
    transform: scale(1.3);
}

.dots {
    position: absolute;
    width: 100%;
    height: 400px;

    overflow: hidden;
}

.dots .v-img {
}
.landing-content {
    position: relative;
    background: transparent;
    height: 100vh;
}

.landing-content .img {
    padding: 0;
    margin: 0;
    z-index: 2;
}
.landing-content .img * {
    background-position: bottom;
}

.skills {
    position: absolute;
    z-index: 3;
    height: 400px;
    width: 40%;
    padding: 2em;
    bottom: 100px;
}

/* Social media ++++++++++++++++++++++++++++++++++*/
.social-media {
    height: 35vh;
    width: 100%;
    background: black;
    overflow: hidden;
    padding: 0;
    margin: 0;
}
.social-media .row {
    height: 100%;
}

.social-media i {
    font-size: 8vh;
}
/* UI ====+++=++=====++++++======================== */
.ui-portfolio {
}
.ui-portfolio .row {
    width: 80%;
}
.ui-portfolio .row .col {
    position: relative;
}

/* Projects ======================================== */

.projects-portfolio {
    height: 100%;
    width: 100%;
}
.projects-portfolio .project {
    width: 80%;
}
.projects-portfolio .project p {
    width: 70%;
}
.buttons {
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}
</style>