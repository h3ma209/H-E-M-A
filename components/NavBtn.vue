<template>
    <div class="menu pa-6 " :class="{active:isClicked,'rounded-circle':!isClicked}">
        <div class="btn-container rounded-circle elevation-3" @click="isClicked = !isClicked">
            <div class="text-caption">
                H E M A .
            </div>
        </div>
        <div class="contents" :class="{active:isClicked}">
            <v-list class="pa-5">
                <v-list-item-group>
                    <v-list-item v-for="item,i in links.notLoggedIn" :key="i">
                        <v-list-item-content class="px-5" @click="isClicked = !isClicked">
                            <div class="link my-3 text-h2 text-left">
                                <nuxt-link text :to="item.to">
                                    {{ i+1 }}. {{ item.title }}
                                </nuxt-link>
                            </div>
                        </v-list-item-content>
                    </v-list-item>
                </v-list-item-group>

            </v-list>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isClicked: false,
            links: {
                notLoggedIn: [
                    {
                        icon: 'mdi-apps',
                        title: 'Home',
                        to: '/',
                        active: true,
                    },
                    {
                        icon: 'mdi-chart-bubble',
                        title: 'My CV',
                        to: 'https://github.com/h3ma209/cv-pdf/blob/main/hema-omer-cv.pdf'
                    },
                    {
                        title: 'Portfolio',
                        to: 'https://drive.google.com/file/d/14WyCpHtfpTxASUZq0-SiKzx-y9qw1-N5/view?usp=sharing'
                    },
                    {
                        title: 'Contact Me',
                        to: 'mailto:hema.omer007@gmail.com'
                    },
                ],

            }
        }
    }
}
</script>

<style scoped>
* {
    color: #212a4d !important;
    text-decoration: none !important;
}
.menu {
    float: right;
    height: 70px;
    width: 70px;
    display: grid;
    place-content: center;
    transition: all 0.3s cubic-bezier(0.86, 0, 0.07, 1);
    position: fixed;
    z-index: 9999;
    right: 5vw;
    top: 5vw;
}
.menu.active {
    background: white;
    right: 0vw;
    top: 0vw;
    z-index: 9999;
    width: 100vw;
    height: 100vh;
    position: fixed;
}
.contents {
    opacity: 0;
    visibility: hidden;
    transition: all 0.2s ease-in-out;
}
.contents.active {
    visibility: visible;
    opacity: 1;
}
.btn-container {
    background: white;
    float: right;
    height: 70px;
    width: 70px;
    display: grid;
    place-content: center;
    position: fixed;
    z-index: 9999;
    right: 5vw;
    top: 5vw;
    transition: all 0.3s ease-in-out;
}
.btn-container:hover {
    cursor: pointer;
    background: rgb(236, 236, 236);
}
/* .link {
    background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
    background-repeat: no-repeat;
    background-size: 100% 0.2em;
    background-position: 0 88%;
    transition: all 0.25s ease-in;
    cursor: pointer;
}
.link:hover{
    background-size: 100% 88%;
} */
.link {
    transition: all 0.25s ease-in;
    cursor: pointer;
    background-size: 10% 0.2em;
    background-position: 0 80%;
}
.link:hover {
    background-image: linear-gradient(120deg, #03dac6 0%, #03dac6 100%);
    background-repeat: no-repeat;
    background-size: 100% 0.2em;
    transform: scale(1.15);
    background-position: 0 80%;
}
</style>