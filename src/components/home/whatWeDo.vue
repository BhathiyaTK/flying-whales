<template>
    <v-container class="pb-2 px-0 pt-0">
        <v-layout wrap align-center justify-center row fill-height >
           <v-flex xs12 md3 lg3 class="pa-2">
               <p class="google-font" style="font-size:180%">Mission</p>
               <p class="google-font" style="font-size:110%">{{sefDetails.mission}}</p>

               <!-- <p class="google-font" style="font-size:110%">About different Google technologies</p> -->

                <!-- <span v-for="(item,i) in whatWeDoData" :key="i">
                    <v-tooltip bottom>
                        <template v-slot:activator="{ on }" >
                            <a :href="item.link" target="_blank" flat class="ma-0">
                                <img :src="getImgUrl(item.image)" width="30vh" alt="" srcset="" dark v-on="on">
                            </a> 
                            &nbsp;&nbsp;&nbsp;
                        </template>
                        <span>{{item.TechName}}</span>
                    </v-tooltip>
                </span>
                
                <br><br>

                <v-btn :href="chapterDetails.GDGProgramWebsite" outline target="_blank" round color="#7B1E79" style="text-transform: capitalize;border-radius:5px;text-transform: capitalize;" flat  class="ml-0 google-font hidden-md-and-down" dark>Learn More</v-btn> -->

            </v-flex> 
            <v-flex xs12 md9 lg9 class="pa-3">
                <v-layout row wrap>

                    <v-flex xs6 sm6 md4 lg4 class="text-xs-center pa-2">
                        <!-- <v-icon large style="font-size:300%">chat_bubble</v-icon> -->
                        <v-layout align-center justify-center fill-height = "true">
                             <v-img class="center center"
                             contain="true"
                            :src="require('@/assets/img_/brand/irc.png')"
                            :lazy-src="require('@/assets/img_/brand/irc.png')"
                            width="90%"
                             max-height ="200px">
                            <v-layout
                                slot="placeholder"
                                fill-height
                                align-center
                                justify-center
                                ma-0
                            >
                                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                            </v-layout>
                            </v-img>
                        </v-layout>
                         <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" outline color="#0D0A3F" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Learn More</v-btn>
                        <!-- <p class="google-font" style="font-size:130%">Talks</p> -->
                        <!-- <p class="google-font" style="font-size:110%">Get updated with the latest news and announcements</p> -->
                    </v-flex>

                    <v-flex xs6 sm6 md4 lg4 class="text-xs-center pa-2">
                        <!-- <v-icon large style="font-size:300%">code</v-icon> -->
                         <v-layout align-center justify-center fill-height = "true">
                        <v-img class="center center"
                            contain="true"
                            :src="require('@/assets/img_/brand/onelive.png')"
                            :lazy-src="require('@/assets/img_/brand/onelive.png')"
                            width="auto"
                            max-height ="200px">
                            <v-layout
                                slot="placeholder"
                                fill-height
                                align-center
                                justify-center
                                ma-0
                            >
                                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                            </v-layout>
                            </v-img>
                         </v-layout>
                          <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" outline color="#0D0A3F" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Learn More</v-btn>
                        <!-- <p class="google-font" style="font-size:130%">Codelabs</p> -->
                        <!-- <p class="google-font" style="font-size:110%">Get hands-on experience and guidance from the community members</p> -->
                    </v-flex>

                    <v-flex xs6 sm6 md4 lg4 class="text-xs-center pa-2">
                        <!-- <v-icon large style="font-size:300%">school</v-icon> -->
                          <v-layout align-center justify-center style ="min-height:200px" fill-height = "true">
                            <v-img class="center center"
                                contain="true"
                                :src="require('@/assets/img_/brand/scholarx.png')"
                                :lazy-src="require('@/assets/img_/brand/scholarx.png')"
                                width="auto"
                                max-height ="200px">
                                <v-layout
                                    slot="placeholder"
                                    fill-height
                                    align-center
                                    justify-center
                                    ma-0
                                >
                                    <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                                </v-layout>
                                </v-img>
                            </v-layout>
                             <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" outline color="#0D0A3F" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Learn More</v-btn>
                        <!-- <p class="google-font" style="font-size:130%">Campus Roadshows</p> -->
                        <!-- <p class="google-font" style="font-size:110%">Share knowledge in different Companies, colleges and universities</p> -->
                    </v-flex>

                    <!-- <v-flex xs6 sm6 md3 lg3 class="text-xs-center pa-2">
                        <v-icon large style="font-size:300%">airplay</v-icon>
                        <p class="google-font" style="font-size:130%">Live Viewing Parties</p>
                        <p class="google-font" style="font-size:110%">Share knowledge in different Companies, colleges and universities</p>
                    </v-flex> -->

                </v-layout>
            </v-flex>
        </v-layout>

    </v-container>
</template>

<script>
import whatWeDoData from '@/assets/data/whatWeDoComponentData.json'
import ChapterDetails from '@/assets/data/chapterDetails.json'
import SEFDetails from '@/assets/data/sefHomePage.json'
export default {
    data() {
        return {
            chapterDetails: ChapterDetails,
            whatWeDoData: whatWeDoData,
            sefDetails : SEFDetails
        }
    },
    methods:{
        getImgUrl(url) {
            if(url.length>0){
                return require('@/assets/img/what-we-do/'+url)
            }else{
                return require('@/assets/img/what-we-do/notFound.png')
            }
        },
    }
}
</script>
