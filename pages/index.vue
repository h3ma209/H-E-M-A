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

                    <v-img contain max-height="650" max-width="550" src="https://drive.google.com/file/d/1yfnCrCeuMpyEggGRFqrnGin1zkhrQ_O_/view?usp=sharing"></v-img>
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
        <div class="about">
            <v-row align="center" justify="center">
                <v-col class="desc" cols="5" xs='12'>

                    <h1>
                        About Me
                    </h1>
                    <span></span>
                    <p>
                        Hello There, 👋 I am Hema, full-stack developer with versatile skills, i have been with computers since i was 13 years old,
                        creating and designing and problem solving are my passions, making cool and creative projects was always my goal
                    </p>
                    <p>
                        I have experience of more than 2 years in web development
                        I love using vuetify and bootstrap for frontend,
                        and for backend i use NodeJs and Laravel, and Mysql for database
                    </p>

                </v-col>
            </v-row>
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
                                <v-img :src="ui.img" max-width="350"></v-img>
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
                { title: 'Ford Dealership Redesign', tech: 'Vuetify, NuxtJS', description:'As Ford fanboy i wanted to make a cool design for the 2021 shelby GT500', source:'https://github.com/h3ma209/Ford-dealership', live:'https://gt500.netlify.app/' , img:'https://raw.githubusercontent.com/h3ma209/Ford-dealership/master/thumbnail.png'},
                { title: 'MovieDB', tech: 'Vuetify, NuxtJS, Vuex', description: 'IMDB like movie browsing website you can search for movies and etc.. i used REST API for the movie datas', source: 'https://github.com/h3ma209/MovieDB', live: 'https://moviedbb.netlify.app/', img: 'https://raw.githubusercontent.com/h3ma209/MovieDB/master/Screenshot%20(27).png' },
                { title: 'CRM', tech: 'Bootsrap, VueJS,PHP, Laravel', description: 'Customer relations project i made for SmartMed.com fully secure and responsive for handling customers, contracts, receipts, etc....', source: 'https://github.com/h3ma209/CRM', live: '', img: 'https://raw.githubusercontent.com/h3ma209/CRM/master/Screenshot%20(20).png' },
                { title: '1970 Boss 302', tech: "HTML, CSS, JS, GSAP", description: "the classic legendary 1970 ford mustang boss 302", source: 'https://github.com/h3ma209/Ford-UI', live: 'https://h3ma209.github.io/Ford-UI/', img: 'https://raw.githubusercontent.com/h3ma209/Ford-UI/gh-pages/Screenshot%20(182).png' },
                { title: 'Mobile fashion ecommerce', tech: 'Nuxjs, Vuejs', description: 'A Fashion ecommerce with a cool and simple UI with search and filtering', source: 'https://github.com/h3ma209/mobile-fashion-ecom', live: '', img: 'https://camo.githubusercontent.com/0b89e43464db6e41ca59cb65d8ace2ea5a76f26940a5644ea7c82e7a17abf5b1/68747470733a2f2f63646e2e6472696262626c652e636f6d2f75736572732f353637353133392f73637265656e73686f74732f31353631303431312f6d656469612f33633433633365386131646232316430666234343639626634643731313131312e6a70673f636f6d70726573733d3126726573697a653d38303078363030' },
                { title: 'Mustang UI', tech: 'HTML, CSS', description: 'Made this for my dream car using just html and css', source: 'https://github.com/h3ma209/Mustang-ui', live: 'https://h3ma209.github.io/Mustang-ui/', img: 'https://raw.githubusercontent.com/big-yoshi/mustang-ui/master/assets/ui.png' },
                { title: 'Node job portal', tech: 'Bootstrap, Nodejs, Socket.io, MongoDB', description: 'this was a project i was working on back when i was in 51labs, its a simple job portal ', source: 'https://github.com/h3ma209/node-job-portal', live: '', img: 'https://raw.githubusercontent.com/h3ma209/node-job-portal/master/Screenshot%20(4).png' },
                { title: 'Personal Blog', tech: 'Vuejs, Nodejs, Socket.io', description: 'Its a Real time private blog you can use it as diaries More features are coming I will be fixing the bugs when im done with exams', source: '', live: '', img: 'https://raw.githubusercontent.com/h3ma209/ui-designs-xd/main/blog/Web%201920%20%E2%80%93%201.png' },
                { title: 'Boss 302', tech: "HTML, CSS, JS, GSAP", description: "My all time favorite classic muscle car", source: 'https://github.com/h3ma209/cool-simple-scroll-magic', live: 'https://h3ma209.github.io/cool-simple-scroll-magic/', img: 'https://raw.githubusercontent.com/h3ma209/cool-simple-scroll-magic/gh-pages/Screenshot%20(183).png' },

            ],
            uis: [
                { title: 'Aryan Post', link: 'https://drive.google.com/file/d/1IjEAujst6hoitpjQyWGXbNON7BQsnOMH/view?usp=sharing', img: 'https://lh3.googleusercontent.com/fife/AAWUweWx7xrBzVlsES_lUPC9xIGGiZPYhCjZ58C5BYelOQ72CSMk5tNBUfwLa2-IozPT9qEQ24d36gZWMqZMKx55BZK--wW1-jgBa_w0r_7lCFnJcXJGZsPs3ONn3foj6ftbyIOgCAcpNMMHGuG64c0HEqzrPW07slyB2H_2iz_sgBVyLw_Ws-EDY5eF9EE1xQTAg5lufyPAEFOOjpx6yufRm9-WGSoYZBKy2PAhR0cI9_4MWSTInD9hMQv1Lic_9y6ULAQGmzEV-i08QojgvzyHb0bnPghDO-cjKqXDHB2pVwp7who1zCYtWNsyHUA35tKut7WMtEKjf6kqNbikLY7a_Z-GgWsst9tJNCXleSY-hA7sQenRkzylBw9xZI698-J4JG4-0uTj7Sc6Qfn8Jfgxv7dT6A1U2cuPEc566uT5Q8UlDaN-WGgr57vkp9ToBP-lW_M3-0Wcqcr6bt_5dlPpASVw6WpO2D5uIeYe_fcsS_aHhh2ktbnXw5yM1JdSfwlbpVeg3EZDo7HQikl4YOJnpOpdXDJE9bBszWl70ZlSl-V4tSjYB5m8j0UllyqHHwIrVDIqiweXp2pJOKKkIU88KUddXN1Ne1K1ztLs8rKh0sRb5yJO79tpRvpoSAg5ML6o6zEvw9V-_p4wJ_cmxSEXuxnKPusGne40eIpjrTBd4o162zZdJgOEEirzIzAUQOHOG2nqofwjU66CyuG-Hi31XZ2mYDPkSd2VvHY=w1920-h923-ft' },
                { title: 'Potan', link: 'https://drive.google.com/file/d/19HoGMisaSD9Se74q1-zlBMFuMFBUDLsF/view?usp=sharing', img: 'https://lh3.googleusercontent.com/fife/AAWUweVFulTUuf0zn4ONs6JgpiHeoAuDQ08filQ8fbC0HtmJqbm2G5SgFj7L7hbIdalkUT7T25Fw69Y80oZsnxkZuSUMFKVA13AYWCoMpkxycvGeAK_-PpvGDM2mXJlJRvrvanBz0-ela-j2-OaOrMvZzvIe4X6l7tKRPsacH3LJFGPVELt4RAflvTX4fDMxxqAGuWvAJXuAczDnZVqdctlB-XmZwRB0YUSm5bLOwaUjUSMfEmyPC2B67aIHZK6SFN1wpqbDWHaGaMD54oI5pgwr5Z0fXkOkE1gfkBdLnrh4DWkCcTFv1KT9mfHpDXRsCVlfns7AT66bfNI0aT3KRIvjY7gpHVPzo4S2M9akO41i1iz61xguhF5aIQr5qj9ZmGXDd94niPnKwu2w3_k5oMG5P0Jkl6w-DWnjtvbNVQQ8pSEGsAXaw5HeyzEEJHKU3W8Rbe9XDJJOs9J2s2lPZzhbRL5_SHM60BA5yj42BxmYlhS5Wg21nS7AoxlzwYkwbvq0vuyYjFUJtM9Y4I7SQliDt7guWAECFKdIVMYrq-6SZsUTqisxA6xl2vUrdgHaoyKJ3bj4BZsh0tZ223XH96-Qd5CT5sh-sPZpJHwM94h2Mi1UFNkv-9dJLzHykFHMVYX-I8cSXjhz2TgFpD5g3UJJpVHUd0n4AACNcfT624y9kUhLvezLNeQv6dvWZXEIZ1pZhpgytFSFPjlqW4v0iyBAtNsk2gFVxPZKSWI=w1920-h923-ft' },
                { title: 'Sai2', link: 'https://drive.google.com/file/d/125i8GFcjv8EGoRDBXC2E0crg9uL1TDh0/view?usp=sharing', img: 'https://lh3.googleusercontent.com/fife/AAWUweVvFePGau7agtNd0VaBNi1uXV_UGTA_gIiLiP62Y9xSh8bZwC69zEn7S2WqD-XO1qCVshkUsLTXUp3WREPu95_GnxmshcHWQIpq0W0GVvvZqVlf86uiwfp_GbnqHtBDOI7wKBxb7ytpHftFe-ieSSkgzDRzhEvZ0m2dw_hXXiF0xVS2NK2zsN6Fw35z6myvziWlOerRVpdzjPTxxBRjSA1wDtsC_WsaYcFzIP9MKbbsa5J2_vPU6qdbcNT-gar0AoJBkkK4_LE6cJ4i6wpxbZljaihRq26bTipI5WBVAsZzSsvz9V2KvR5sh67oVrkkAiJ4l_HFsUH3CeetUgL41vQOosaSiynz_cXXi3xtLjuyvC5FJuc-LWpK1wp8cusx89UfMSEz-fbxX2lrkergLRHJSW6HxRtaF4qJQXpyU3bWstBTsf31DE7PGk5ZfmySqKVOl_oS2jrgxeKBNYjGGt5QSx-rzE0S1h7mRGOnKFWyouJcYUJByN3_7m6JrvPJycnQCUf0WNHAloSUTZxz5wyTqEtJVMM5fJRaMS01E4Iagq9VNytCb7G-LvDLSWLfPf1t42XBb-P31dXbgjR6K4AaEdIsatmg4ZJ3MJqI5uhMhNJlljHWhUeY1Q98IbCPOD80KOXG3cwZp52nENxqF8b7vKoUxSFSII066JUgLnE627Ups6Le3H_SrcY8Pu1rzTi_uNvzvLYYXy7HLsfexj8cG95YOFRKCYE=w1920-h923-ft' },
                { title: 'Sardam post', link: 'https://drive.google.com/file/d/1t6eQGWb8GrqxFrvFpGQXmqtahi_5Jc5h/view?usp=sharing', img: 'https://lh3.googleusercontent.com/fife/AAWUweVqVTm5UL77KVQrYbD5cMQLzwsID2CYwqg8SlJGit5--Ej0SXCN6oKjd5Hm-gQrk-5rHEfewOThoicNWakDXppFIfqvbE9gN9SyXskmwBbCcjmpAxO6mbbCZERnkETCTiIAkM5y_nOvp9S7mFdWiRYxWBK--yIUwZvW4LhBgtva6P20-gJdw-jqli0Lg2Teac8p5weqHi35Iddbb7d8kEVKml8KR3zibmPzT2GO2JJ3j62YSyPCchkhU0fjiUOHEpJhvfxSmhDmkuoBYY4b7-V-s4k-EBJErj6K_YKt7oj97iHRSJ586uaJSFgRjVmUG0_8r2t3C6eobAaXDhTLyIo0RuNCMCP2td5qHuf8S9NNKTTLYL9BHJpJKFkdEooN1zMikqZZTdmcpLMZlZdnT5Se8MctVCdCGT8AJoxtIIw_sgRX4XngDh6wcHvw8QMF1by1yHMjONQGo55SDM2_iWsN_rYjLJD4j3lGoZEb4QwP0LorJsAcFKpyMEKtFnm3e88aocrDLnf5CDDUiuauKwA-jhPFfqFXxqfKKnV_KtvaBD0hnxzeaQ2s-uWgmkMJMpSWMNbGE5UCx13Ll0mlwMLhNR4iR22sKyh94c4xjYraGVLNtYmaJQIpyZfkg3Vz6A0SG5PIVswZxoFc9ZnkomezKHmyOB1ut6qfKsiFWWi3XAYBt1QRs2XfUIdlUpp5lj5DusINKcy1KxNaIdqo3mYloKZSpoUuKYg=w1920-h923-ft' },



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
    },
    methods: {}


}
</script>

<style scoped>
.whitespace {
    height: 30vh;
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
    display: none;
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

/* About Me ++++++++++++++++++++++++++++++++++*/
.about {
    height: 100vh;
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
    font-weight: 300;
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