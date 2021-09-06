<template>
    <v-row justify="center" align="center" class="landing">

        <v-col class="d-grid" align="center">
            <v-sheet class="mt-12">
                <span>I’m <span class="primary--text">Hema.</span> Fullstack developer and a Ui/Ux designer</span>
            </v-sheet>
            <v-spacer></v-spacer>
            <v-row class="skills" align="center" justify="center">
                <v-row no-gutters style="height: 250px;" class="v-row">
                    <!-- <v-col v-for="align in ['start','center','end']" :key="align" :align-self="align">
                        <v-card class="pa-2" outlined tile>
                            One of three columns
                        </v-card>
                    </v-col> -->
                    <v-col align-self="start">
                        <div class="pa-3 rounded-pill" outlined tile >Fullstack developer</div>
                    </v-col>
                    <v-spacer></v-spacer>

                    <v-col align-self="start"  class="justify-end">
                        <div class="pa-3 rounded-pill " outlined tile >Fullstack developer</div>
                    </v-col>
                    <v-col align-self="end">
                        <div class="pa-3 rounded-pill " outlined tile >Fullstack developer</div>
                    </v-col>
                </v-row>
                <div class="purple-blur">

                </div>
            </v-row>
        </v-col>
    </v-row>
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
.landing {
    height: 100%;
    width: 100%;
    overflow: hidden;
    position: relative;
}

.skills {
    position: relative;
}
.skills .v-row {
    position: absolute;
    width: 60%;
    align-self: center;
    justify-self: center;
    z-index: 9999;
}

.skills .v-row .col div{
    background: white;
}
.v-sheet span {
    font-size: 44px;
    font-weight: normal;
}

.purple-blur {
    width: 50%;
    height: 500px;
    bottom: -130px;
    position: relative;
    align-self: start !important;
    background: #150dfb;
    filter: blur(1000px);
    opacity: 0.5;
    border-radius: 50%;
}
</style>