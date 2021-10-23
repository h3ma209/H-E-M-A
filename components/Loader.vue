<template>
    <div class='loader'>
        <div class='objects'>
            <div class='rectangle' id='r1'>
            </div>
            <div class='rectangle' id='r2'>
            </div>
            <div class='rectangle' id='r3'>
            </div>
            <div class='rectangle' id='r4'>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    setup() {

    },
}
</script>
<style scoped>
body,html{
    
}
.loader {
    height: 100vh;
    width: 100%;
    background: white;
    display: grid;
    place-items: center;
    position: absolute;
    z-index: 999999999999;
    top: 0 !important;
    left: 0;
}
</style>