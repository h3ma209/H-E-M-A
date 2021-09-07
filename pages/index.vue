<template>
    <div class="page">
        <div class="landing">
            <v-img src="/white_eclipse.svg" class="eclipse" max-height="150px">

            </v-img>
            <v-row no-gutter class="text-center mt-14" align="center" justify="center" style="top:100px">
                <v-sheet>
                    <h1 class="font-weight-regular">I'm <span class="primary--text font-weight-regular">Hema</span>, Im a Fullstack developer and a UI/UX designer</h1>
                </v-sheet>
            </v-row>
            <v-row class="dots">

            </v-row>
            <v-row class="landing-content" align="end" justify="center">
                <v-row no-gutters  class="skills">
                    
                    <v-col align-self="start" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            Front-end
                        </v-card>
                    </v-col>
                    <v-col align-self="end" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            Front-end
                        </v-card>
                    </v-col>
                    
                    <v-col align-self="center" class="">
                        <v-card class="pa-3 font-weight-bold rounded-pill text-center" outlined tile>
                            Front-end
                        </v-card>
                    </v-col>
                </v-row>
                
                <div class="img">
                    <v-img contain lazy-src="@/assets/landing.png" max-height="650" max-width="550" src="/landing.png"></v-img>
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
.eclipse{
    position: absolute;
    top: 0;
    left: 0;
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
    transform: scale(1.2);
}
.landing-content {
    position: relative;
    overflow: hidden;
    height: 100vh;
}

.landing-content .img {
    padding: 0;
    margin: 0;
    z-index: 2;
}

.skills {
    position: absolute;
    z-index: 3;
    height: 400px;
    width: 650px;
    padding: 2em;
}
</style>