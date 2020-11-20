<template>
    <v-app id="inspire">
        <v-app-bar app
                   color="white"
                   flat
                  inverted-scroll>
            
            <v-tabs centered
                    class="ml-n9"
                    color="teal darken-1"
                    show-arrows>
                <v-tabs-slider color="teal lighten-3"></v-tabs-slider>
                <v-tab v-for="link in links"
                       :to="link.href"
                       replace
                       >
                    {{ link.name }}
                </v-tab>
            </v-tabs>
                        
        </v-app-bar>
        
        <v-main class="grey lighten-3" dark>
            <section id="About">
                <v-container class="pa-3">
                    <h1>aswin dinesh.</h1>
                    <v-row>
                        <v-col class=" text-center" cols="12"
                               sm="6">
                            <v-avatar size="225" center>
                                <img src="https://avatars1.githubusercontent.com/u/32993764?s=460&u=06a56c94ba84398657724c662cfc589bccc20b86&v=4" />
                            </v-avatar>
                        </v-col>
                        <v-col cols="12"
                               sm="6">
                            <p>Developer | Tech Enthusiast | Occasional Writer</p>
                            <p>Ardent coder. Loves to solve problems. Contributed to Open Source Projects. Tech Enthusiast. Worked in various python based projects. Winner of Best Automation Hack at Hack Camp 2020.</p>
                            <p>Loves to build PC from scratch, experiment with various linux distros and other OSes.</p>
                            <p>For humanly activities, I love to listen to music and binge on to some series.</p>
                        </v-col>
                    </v-row>
                </v-container>
            </section>

            <section id="Education">
                <v-container class="pa-3">
                    <h2>Education</h2>
                    <v-row>
                        <v-col cols="12"
                               sm="4">
                            <h3>NSS College of Engineering</h3>
                            <h5> B.Tech, Computer Science and Engineering</h5>
                            <p> 6.74 CGPA - August 2016 - July 2020</p>
                        </v-col>
                        <v-col cols="12"
                               sm="4">
                            <h3>Kendriya Vidyalaya, Ernakulam</h3>
                            <h5>12th,PCM with Computer Science</h5>
                            <p>92.4% - May 2016</p>
                        </v-col>
                        <v-col cols="12"
                               sm="4">
                            <h3>Kendriya Vidyalaya, Ernakulam</h3>
                            <h5>10th</h5>
                            <p>9.8 CGPA - May 2014</p>
                        </v-col>
                    </v-row>
                </v-container>
            </section>
            <section id="Projects">
                <v-container class="pa-3">
                    <v-row justify="space-around">
                        <v-col cols="12"
                               sm="6">
                            <h2>Projects</h2>

                            <v-list shaped class="grey lighten-3">
                                <v-list-item-group v-model="selectedItem"
                                                   color="grey darken-1">
                                    <v-list-item v-for="(item, i) in project"
                                                 :key="i"
                                                 :href="item.href">
                                        <v-list-item-content>
                                            <v-list-item-title v-text="item.text"></v-list-item-title>
                                        </v-list-item-content>
                                    </v-list-item>
                                </v-list-item-group>
                            </v-list>
                        </v-col>

                        <v-col cols="12"
                               sm="6">
                            <h2>Tech Stack</h2>
                            <v-breadcrumbs :items="skills" divider="|">
                            </v-breadcrumbs>
                        </v-col>

                    </v-row>
                </v-container>
            </section>

            <section id="Activities">
                <v-container class="pa-3">
                    <v-row>
                        <v-col cols="12"
                               sm="6">
                            <h2>Activities</h2>
                            <p>Winner of Best Automation Hack at HackCamp 2020, Kochi</p>
                            <p>Contributed to IndicNLP at PyCon 2019, Chennai</p>
                        </v-col>
                        <v-col cols="12"
                               sm="6">
                            <h2>Courses</h2>
                            <p>Python for Everybody - Specialisation - Coursera</p>
                            <p>Introduction to Automata, Languages and Computation - NPTEL</p>
                        </v-col>
                    </v-row>
                </v-container>
            </section>

            <section id="Contact">
                <v-container>
                    <v-footer dark
                              padless>
                        <v-card class="flex"
                                flat
                                tile>
                            <v-card-title class="teal lighten-3">
                                <strong class="subheading">Feel free to ping!</strong>

                                <v-spacer></v-spacer>

                                <v-btn v-for="icon in icons"
                                       :key="icon.id"
                                       :href="icon.href"
                                       class="mx-1"
                                       dark
                                       icon>
                                    <v-icon size="24px">
                                        {{ icon.name }}
                                    </v-icon>
                                </v-btn>
                            </v-card-title>

                            <v-card-text class="py-2 white--text text-center">
                                {{ new Date().getFullYear() }} - <strong>Vuetify</strong>
                            </v-card-text>
                        </v-card>
                    </v-footer>
                </v-container>
            </section>
        </v-main>
    </v-app>
</template>

<script>
    export default {
        data: () => ({
            links: [
                { name: 'Aswin Dinesh', href: '#About', id: 1 },
                { name: 'Education', href: '#Education', id: 2 },
                { name: 'Projects and Tech Stacks', href: '#Projects', id: 3 },
                { name: 'Activities and Courses', href: '#Activites', id: 4 },
                { name: 'Contact', href: '#Contact', id: 5 },
            ],
            skills: [
                { text: 'Python', id: 1 },
                { text: 'C', id: 2 },
                { text: 'PHP', id: 3 },
                { text: 'MySQL', id: 4 },
                { text: 'VueJS', id: 5 },
                { text: 'HTML', id: 6 },
                { text: 'Linux', id: 7 },
                { text: 'UiPath', id: 8 },
                { text: 'CSS', id: 9 },
                { text: 'JS', id: 10 },
                { text: 'Adobe Audition', id: 11 },
                { text: 'Adobe Premiere Pro', id: 12 },
            ],
            project: [
                { text: 'A Movie Recommendation System', href: 'https://github.com/aswindinesh/movieRecommend', id: 1 },
                { text: 'Basic Image Classification using TensorFlow Keras on MNIST Dataset.', href: 'https://github.com/aswindinesh/imageClassification', id: 2 },
                { text: 'Movie Name Scraper - Scrapes list of all movies made from the year 1986-2021.', href: 'https://github.com/aswindinesh/wikiMovies', id: 3 },
                { text: 'Office Appointment System', href: 'https://github.com/aswindinesh/appointmentfrontend', id: 4 },
                { text: 'FOCE - Food Observation and Calorie Estimation', href: 'https://foce.theabstraction.co/', id: 5 },
            ],
            selectedItem: 1,
            items: [
                { text: 'Real-Time', icon: 'mdi-clock' },
                { text: 'Audience', icon: 'mdi-account' },
                { text: 'Conversions', icon: 'mdi-flag' },
            ],
            icons: [
                { name: 'mdi-gmail', href: 'mailto:aswin11.dinesh@gmail.com', id: 1 },
                { name: 'mdi-twitter', href:'https://twitter.com/_aswindinesh',id:2}, 
                { name: 'mdi-linkedin', href:'https://www.linkedin.com/in/aswindinesh/',id:3},
            ],

        }),
    }
</script>