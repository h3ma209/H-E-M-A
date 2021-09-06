<template>
    <v-sheet>
        <span>{{text}}</span>
    </v-sheet>
</template>

<script>
export default {
    props:['text']
}
</script>

<style scoped>
span{
    font-size: 54px;
}
</style>