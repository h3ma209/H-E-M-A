<template>
    <div class="page">
        <div class="landing">
            <v-img src="/white_eclipse.svg" class="eclipse" max-height="150px"></v-img>
            <v-row no-gutter class="text-center mt-14" align="center" justify="center">
                <h1 class="font-weight-regular mt-12">I'm <span class="primary--text font-weight-regular">Hema</span>, Im a Fullstack developer and a UI/UX designer</h1>
            </v-row>
            <v-row class="dots" align="center" justify="center">
                <v-col align="center" justify="center">
                    <v-img src="/dot.svg" max-width="60%" style="opacity:0.5"></v-img>
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

    </div>

</template>

<script>
import Header from "@/components/Typo/Header.vue"


export default {
    components: {
        Header
    },
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
.landing {
    overflow: hidden;
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
    bottom: 30vh;
}

.dots .v-img{

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
}
</style>