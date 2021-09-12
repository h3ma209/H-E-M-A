<template>
    <v-row class="project mb-14 mt-14" justify="space-between">
        <v-col class="d-flex align-center " cols="6">
            <v-card class="text-left  elevation-0 ">
                <v-card-title>
                    <h1 class="mb-4">{{project.title}}</h1>
                </v-card-title>
                <v-card-subtitle><span>{{project.tech}}</span></v-card-subtitle>
                <v-card-text class="">
                    <p>{{project.description}}</p>
                </v-card-text>

                <v-card-actions>
                    <v-btn class="rounded-pill elevation-0 primary pa-5">Live</v-btn>
                    <v-btn class="rounded-pill elevation-0 pa-5" outlined>Source</v-btn>
                </v-card-actions>
            </v-card>
        </v-col>
        <v-col cols="6">
            <v-row class="elevation-1 rounded-t-lg rounded-b-lg">
                <v-col class="d-flex align-center rounded-t-lg" style="background:#E7E7E7">
                    <v-card class="pa-2 rounded-circle mr-1 ml-1 elevation-0 " style="background:red" tile></v-card>
                    <v-card class="pa-2 rounded-circle mr-1 ml-1 elevation-0 " style="background:green" tile></v-card>
                    <v-card class="pa-2 rounded-circle mr-1 ml-1 elevation-0 " style="background:yellow" tile></v-card>
                </v-col>
                <v-col class="pa-0 ma-0">
                    <v-img class="rounded-b-lg" lazy-src="https://picsum.photos/id/11/10/6" max-height="350" style="background:red;" :src='project.img'>
                    </v-img>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script>
export default {
    props: ['project']
}
</script>
<style scoped>
</style>