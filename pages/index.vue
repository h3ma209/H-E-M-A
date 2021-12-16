<template>
    <div class="page">

        <!-- <v-overlay z-index="999999999" :value="overlay">
            <v-card>
                <v-carousel v-model="model">
                    <v-carousel-item v-for="(ui, i) in uis" :key="i">
                        <v-img :src="ui.img" contain max-width="600">

                        </v-img>
                        
                    </v-carousel-item>
                </v-carousel>
            </v-card>
            <v-btn @click="overlay = !overlay" class="error">Close</v-btn>
        </v-overlay> -->

        <div class="landing">
            <v-img src="/white_eclipse.svg" class="eclipse" max-height="150px"></v-img>
            <v-row no-gutter class="text-center mt-14 landing-title" align="center" justify="center">
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

                    <v-img contain max-height="700"  min-height="300"  src="/hema-bw.png"></v-img>
                </div>
                <div class="purple-blur"></div>
            </v-row>

        </div>

        <div class='about'>

            <div class='desc'>
                <h1>
                    About Me
                </h1>
                <span></span>
                <p>
                    Hello There, 👋 I am Hema, full-stack developer with versatile skills,

                    I have experience of more than 2 years in web development
                    I love using vuetify and bootstrap for frontend,
                    and for backend i use NodeJs and Laravel, and Mysql for database
                </p>
            </div>
        </div>

        <div class="whitespace"></div>
        <h1 class="text-center mb-14 mt-14">UIs</h1>
        <div class="ui-portfolio d-flex justify-center align-center mb-6 pa-2">

            <v-row align="center" justify="center">
                <v-col class="pa-1 ma-4 d-flex justify-center align-center" lg='3' xs='1' v-for="ui,i in uis" :key="i">
                    <!-- <v-img :src="ui.img" max-height="300"></v-img> -->
                    <v-hover>
                        <template v-slot:default="{ hover }">
                            <v-card class="mx-auto">
                                <v-img :src="ui.img" max-width="350" lazy-src="https://media.istockphoto.com/photos/abstract-3d-art-background-with-curve-shape-holographic-color-picture-id1266776339?b=1&k=20&m=1266776339&s=170667a&w=0&h=EMXVNKMTMfoKMTXBc__MBaKTMszC8XskMbObvghyRBw=">
                                    <template v-slot:placeholder>
                                        <v-row class="fill-height ma-0" align="center" justify="center">
                                            <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                                        </v-row>
                                    </template>
                                </v-img>

                                <v-fade-transition>
                                    <v-overlay v-if="hover" absolute color="#036358">
                                        <v-btn @click="overlay = !overlay" :href="ui.link" target="_blank" class="primary rounded-pill">See Details</v-btn>
                                    </v-overlay>
                                </v-fade-transition>
                            </v-card>
                        </template>
                    </v-hover>
                </v-col>
            </v-row>
        </div>
        <div class="whitespace"></div>
        <h1 class="text-center mb-14 mt-14">Projects</h1>

        <div class="projects-portfolio pr-4 pl-4" align='center' justify="space-between">
            <Project v-for="project,i in projects" :key="i" :project="project"></Project>
        </div>
        <div class="whitespace"></div>
        <div class="social-media">
            
                    <v-img id="prlx" eager  class="fill-height ma-0 pa-0" src="https://wallpaper.si/wp-content/uploads/2017/03/27-02-17-forest-landscape-pictures13569.jpg" alt="">
                        <!-- <v-row class="ma-0 pa-14 text-center" align="center" justify="center" style="background:green;">
                            <v-col class="pa-0 mx-1"  id="codepen" >
                                <v-btn width="150" height="150">
                                    <v-icon>fab fa-codepen</v-icon>
                                </v-btn>
                            </v-col>
                            <v-col class="pa-0 mx-1"  id="twitter">
                                <v-btn width="150" height="150" >
                                    <v-icon>fab fa-twitter</v-icon>
                                </v-btn>
                            </v-col>
                            <v-col class="pa-0 mx-1"  id="dribble" >
                                <v-btn max-width="150" height="150" width="150">
                                    <v-icon>fab fa-dribbble</v-icon>
                                </v-btn>
                            </v-col>
                            <v-col class="pa-0 mx-1"  id="github">
                                <v-btn width="150" height="150">
                                    <v-icon>fab fa-github</v-icon>
                                </v-btn>
                            </v-col>
                        </v-row> -->
                        <v-row justify="center" align="center" class="text-center fill-height" no-gutters id="social-accounts">
                            <v-col class="fill-height d-flex flex-column align-center justify-center" lg="3"    >
                                <v-btn width="150" height="150" id="codepen" target="_blank" href="https://codepen.io/fugi">
                                    <v-icon>fab fa-codepen</v-icon>
                                </v-btn>

                            </v-col>
                            <v-col class="fill-height d-flex flex-column align-center justify-center" lg="3"    >
                                <v-btn width="150" height="150" id="twitter" target="_blank" href="https://twitter.com/H3ma209">
                                    <v-icon>fab fa-twitter</v-icon>
                                </v-btn>
                            </v-col>
                            <v-col class="fill-height d-flex flex-column align-center justify-center" lg="3"    >
                                <v-btn max-width="150" height="150" id="dribble" width="150" target="_blank" href="https://dribbble.com/hema209">
                                    <v-icon>fab fa-dribbble</v-icon>
                                </v-btn>
                            </v-col>
                            <v-col class="fill-height d-flex flex-column align-center justify-center" lg="3"    >
                                <v-btn width="150" height="150" id="github"  target="_blank" href="https://github.com/h3ma209">
                                    <v-icon>fab fa-github</v-icon>
                                </v-btn>
                            </v-col>
                        </v-row>
                    </v-img>
                
                <!-- <v-col class="fill-height pa-0">
                    <v-row justify="center" align="center" class="fill-height">
                        <v-card max-height="400" max-width="700" width="400" height="700" class="pa-12">
                            <v-card-title class="mb-7 pa-0">
                                Contact me
                            </v-card-title>
                            <v-card-content class="mb-7">
                                <v-text-field label="Email">
                                </v-text-field>
                                <v-text-field label="Message">
                                </v-text-field>
                            </v-card-content>
                            <v-card-actions>
                                <v-btn class="rounded-pill pa-4 ma-0 elevation-0 primary" flat>
                                    Send
                                </v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-row>
                </v-col> -->
            </v-row>
        </div>

    </div>

</template>

<script>
import Header from "@/components/Typo/Header.vue"
import Project from "@/components/Project.vue"
import gsap from 'gsap'


export default {
    components: {
        Header,
        Project
    },
    data() {
        return {
            model: 0,
            projects: [
                { title: 'Ford Dealership', tech: 'Vuetify, NuxtJS', description: 'As Ford fanboy i wanted to make a cool design for the 2021 shelby GT500', source: 'https://github.com/h3ma209/Ford-dealership', live: 'https://gt500.netlify.app/', img: 'https://raw.githubusercontent.com/h3ma209/Ford-dealership/master/thumbnail.png' },
                { title: 'MovieDB', tech: 'Vuetify, NuxtJS, Vuex', description: 'IMDB like movie browsing website you can search for movies and etc.. i used REST API for the movie datas', source: 'https://github.com/h3ma209/MovieDB', live: 'https://moviedbb.netlify.app/', img: 'https://raw.githubusercontent.com/h3ma209/MovieDB/master/Screenshot%20(27).png' },
                { title: 'CRM', tech: 'Bootsrap, VueJS,PHP, Laravel', description: 'Customer relations project i made for SmartMed.com fully secure and responsive for handling customers, contracts, receipts, etc....', source: 'https://github.com/h3ma209/CRM', live: '', img: 'https://raw.githubusercontent.com/h3ma209/CRM/master/Screenshot%20(20).png' },
                { title: '1970 Boss 302', tech: "HTML, CSS, JS, GSAP", description: "the classic legendary 1970 ford mustang boss 302", source: 'https://github.com/h3ma209/Ford-UI', live: 'https://h3ma209.github.io/Ford-UI/', img: 'https://raw.githubusercontent.com/h3ma209/Ford-UI/gh-pages/Screenshot%20(182).png' },
                { title: 'fashion ecommerce', tech: 'Nuxjs, Vuejs', description: 'A Fashion ecommerce made only for mobile with a cool and simple UI with search and filtering', source: 'https://github.com/h3ma209/mobile-fashion-ecom', live: '', img: 'https://camo.githubusercontent.com/0b89e43464db6e41ca59cb65d8ace2ea5a76f26940a5644ea7c82e7a17abf5b1/68747470733a2f2f63646e2e6472696262626c652e636f6d2f75736572732f353637353133392f73637265656e73686f74732f31353631303431312f6d656469612f33633433633365386131646232316430666234343639626634643731313131312e6a70673f636f6d70726573733d3126726573697a653d38303078363030' },
                { title: 'Mustang UI', tech: 'HTML, CSS', description: 'Made this for my dream car using just html and css', source: 'https://codepen.io/fugi/full/pogBzBJ', live: 'https://h3ma209.github.io/Mustang-ui/', img: 'https://raw.githubusercontent.com/big-yoshi/mustang-ui/master/assets/ui.png' },
                { title: 'Node job portal', tech: 'Bootstrap, Nodejs, Socket.io, MongoDB', description: 'this was a project i was working on back when i was in 51labs, its a simple job portal ', source: 'https://github.com/h3ma209/node-job-portal', live: '', img: 'https://raw.githubusercontent.com/h3ma209/node-job-portal/master/Screenshot%20(4).png' },
                { title: 'Personal Blog', tech: 'Vuejs, Nodejs, Socket.io', description: 'Its a Real time private blog you can use it as diaries More features are coming I will be fixing the bugs when im done with exams', source: '', live: '', img: 'https://raw.githubusercontent.com/h3ma209/ui-designs-xd/main/blog/Web%201920%20%E2%80%93%201.png' },
                { title: 'Boss 302', tech: "HTML, CSS, JS, GSAP", description: "My all time favorite classic muscle car", source: 'https://github.com/h3ma209/cool-simple-scroll-magic', live: 'https://h3ma209.github.io/cool-simple-scroll-magic/', img: 'https://raw.githubusercontent.com/h3ma209/cool-simple-scroll-magic/gh-pages/Screenshot%20(183).png' },
            ],
            uis: [
                { title: 'Aryan Post', link: 'https://drive.google.com/file/d/1IjEAujst6hoitpjQyWGXbNON7BQsnOMH/view?usp=sharing', img: 'https://github.com/h3ma209/ui-designs-xd/blob/main/aryan-post-thumbnail.jpg?raw=true' },
                { title: 'Potan', link: 'https://drive.google.com/file/d/19HoGMisaSD9Se74q1-zlBMFuMFBUDLsF/view?usp=sharing', img: 'https://github.com/h3ma209/ui-designs-xd/blob/main/potan-thumbnail.jpg?raw=true' },
                { title: 'Sai2', link: 'https://drive.google.com/file/d/125i8GFcjv8EGoRDBXC2E0crg9uL1TDh0/view?usp=sharing', img: 'https://github.com/h3ma209/ui-designs-xd/blob/main/sai-thumbnail.jpg?raw=true' },
                { title: 'Sardam post', link: 'https://drive.google.com/file/d/1t6eQGWb8GrqxFrvFpGQXmqtahi_5Jc5h/view?usp=sharing', img: 'https://github.com/h3ma209/ui-designs-xd/blob/main/sardam-post-thumbnail.jpg?raw=true' },
                { title: 'fashion ecom', link: 'https://drive.google.com/file/d/10Yt0LfsXYloVN9LaiToI-0w3Mo1X4OTa/view?usp=sharing', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15610411/media/3c43c3e8a1db21d0fb4469bf4d711111.jpg?compress=1&resize=800x600' },
                { title: 'car dealership', link: 'https://dribbble.com/shots/15527004-car-dealership', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527004/media/991a173559cb2938f3ccccc242a2095f.jpg?compress=1&resize=800x600' },
                { title: 'roy jones jr', link: 'https://dribbble.com/shots/14548447-roy-jones-jr', img: 'https://cdn.dribbble.com/users/5675139/screenshots/14548447/media/bc10463e52e08c6fa9946adf301983aa.jpg?compress=1&resize=1600x1200' },
                { title: 'bmw m5 1', link: 'https://dribbble.com/shots/15527090-simple-car-dealership-website', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15527090/media/1a6cf7d0bc3ba48442e948e754e99e2a.jpg?compress=1&resize=800x600' },
                { title: 'adept gen', link: 'https://github.com/h3ma209/ui-designs-xd/tree/main/adept', img: 'https://raw.githubusercontent.com/h3ma209/ui-designs-xd/main/adept/Web%201920%20%E2%80%93%203.png' },
                { title: 'boss 302', link: 'https://dribbble.com/shots/13449948-Ford-Mustang-GT-Boss-302', img: 'https://cdn.dribbble.com/users/5675139/screenshots/13449948/media/5291b3364e8acd10f244a764339561f0.png?compress=1&resize=800x600' },
                { title: 'gt 350', link: 'https://dribbble.com/shots/13645399-Ford-Mustang-GT350', img: 'https://cdn.dribbble.com/users/5675139/screenshots/13645399/media/41a1ab7c67bf4f4904e57169122555aa.png?compress=1&resize=800x600' },
                { title: 'mike tyson', link: 'https://dribbble.com/shots/14543140-Mike-Tyson', img: 'https://cdn.dribbble.com/users/5675139/screenshots/14543140/media/b8ac26d608313121ab147e8ef7b1f618.png?compress=1&resize=800x600' },
                { title: 'biker jacket store', link: 'https://dribbble.com/shots/15129742-Biker-leather-jacket-store', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15129742/media/fda768518f6102d1b81c0406d6aeca45.jpg?compress=1&resize=800x600' },
                { title: 'sai1', link: 'https://drive.google.com/file/d/1FvO1mz3p-_cPc9Gy9e9HTpufsl3Egu57/view?usp=sharing', img: 'https://cdn.dribbble.com/users/5675139/screenshots/15423495/media/ab5b27da80c12f788b6427f9d5423361.png?compress=1&resize=800x600' },
            ],
            overlay: false,
        }
    },
    created() {
    },
    mounted: function () {
        var about = gsap.timeline({
            scrollTrigger: {
                trigger: ".about",
                start: "50px bottom",
                end: "300px center",
                // markers: { startColor: "green", endColor: "red", fontSize: "12px" }
            }
        });

        about.from('.about h1', { opacity: 0, duration: 1 })
            .from('.about span', { opacity: 0, duration: 1, width: 0 })
            .from('.about p', { opacity: 0, duration: 1 });
    },
    methods: {
    }
}
</script>

<style scoped>
*{
    scroll-behavior: smooth;
}
.whitespace {
    height: 30vh;
}
.v-parallax__content {
    padding: 0 !important;
}

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
    width: 100%;
    background: black;
    
    padding: 0;
    margin: 0;
}
.social-media .row {
    height: 100%;
}

.social-media #prlxs .v-parallax__content{
    padding: 0 0 !important;
}

.social-media i {
    font-size: 8vh;
}
.social-media #prlx #social-accounts {
    
}
.social-media #social-accounts * {
    transition: all .5 ease-in-out;
}

.social-media #social-accounts .col:nth-child(1){
    background: rgba(0, 0, 0, 0.9);
}

.social-media #social-accounts .col:nth-child(2){
    background: rgba(94, 124, 226,0.9);
    }
.social-media #social-accounts .col:nth-child(3){
    background: rgba(255, 61, 109,0.9);
}
.social-media #social-accounts .col:nth-child(4){
    background: rgba(255, 255, 255,0.9);
}

.social-media #social-accounts #twitter {
    background: white;
    
    color: #5e7ce2;
}
.social-media #social-accounts #twitter:hover,
#twitter:active {
    background: #5e7ce2;
    color: white;
}

.social-media #social-accounts #dribble {
    background: white;
    color: rgb(255, 61, 109);
}
.social-media #social-accounts #dribble:hover,
#dribble:active {
    background: #ff3d6d;
    color: white;
}

.social-media #social-accounts #codepen {
    background: white;
    color: black;
}
.social-media #social-accounts #codepen:hover,
#codepen:active {
    background: black;
    color: white;
}

.social-media #social-accounts #github {
    background: white;
    color: #313131;
}
.social-media #social-accounts #github:hover,
#github:active {
    background: #313131;
    color: white;
}
/* About Me ++++++++++++++++++++++++++++++++++*/
.about {
    height: 150vh;
    width: 100%;
    background: #0b090a;
    display: grid;
    position: relative;
}
.about .desc {
    color: #fff;
    width: 55%;
    align-self: center;
    justify-self: start;
    position: absolute;
    left: 8em;
}
.about .desc h1 {
    font-size: 65px;
    font-weight: 400;
    line-height: 100px;
}
.about .desc span {
    height: 8px;
    width: 150px;
    background: white;
    display: block;
    margin: 5px 0px 20px 0;
}
.about .desc p {
    font-size: 26px;
    font-weight: 300;
}

@media only screen and (max-width: 500px) {
    .landing {
    }
    .landing h1 {
        font-size: 30px;
        max-width: 80%;
    }

    .skills {
        width: 100%;
    }
    .about .desc {
        width: 85%;
        left: 30px;
    }
    .about .desc h1 {
        font-size: 30px;
        line-height: 70px;
    }
    .about .desc span {
        width: 70px;
        height: 5px;
    }
    .about .desc p {
        font-size: 17px;
    }
    .social-media{
        height: 120vh;
    }
    .social-media #social-accounts {
        height: 100%;
        
    }
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
