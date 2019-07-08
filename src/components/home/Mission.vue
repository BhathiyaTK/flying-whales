<template>
    <v-container class="pa-0 white--text">
        <v-layout wrap align-center justify-center row fill-height class="my-1" >
            <v-flex xs12 sm5 md5 lg5 >
                <v-img position = 'center center'
                    :src="require('@/assets/img_/group.jpg')"
                    :lazy-src="require('@/assets/img_/group.jpg')"
                    width="96%">
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
            </v-flex>
           <v-flex xs12 sm7 md7 lg7 class="pa-2 py-4 px-3">
               <p class="google-font" style="font-size:155%">Mission</p>
               <p class="google-font" style="font-size:130%">
                   {{sefDetails.mission}}
               </p>
               <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" outline color="white" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Learn More</v-btn>
               &nbsp;
               <!-- <v-btn :href="chapterDetails.socialLinks[0].link" target="_blank" outline color="white" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Facebook Page</v-btn> -->
                <br><br>
               <!-- <router-link to="/about" class="google-font" style="text-decoration:none;color:white">Learn More about SEF</router-link> -->
            </v-flex> 
           
        </v-layout>

    </v-container>
</template>

<script>
import ChapterDetails from '@/assets/data/chapterDetails.json'
import SEFDetails from '@/assets/data/sefHomePage.json'
export default {
    data() {
        return {
            chapterDetails: ChapterDetails,
             sefDetails : SEFDetails
        }
    },
}
</script>
