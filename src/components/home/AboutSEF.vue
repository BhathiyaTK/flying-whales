<template>
    <v-container class="pa-0">
        <v-layout wrap align-center justify-center row fill-height class="my-3" >
           <v-flex xs12 md12 lg12 class="pa-2">
               <p class="google-font" style="font-size:155%">Brief introduction about us</p>
               <p class="google-font" style="font-size:125%; color : #0D0A3F">
                   {{sefDetails.BriefIntroTop}}
               </p>
               <p class="google-font" style="font-size:110%;">
                   {{sefDetails.BriefIntroBtm}}
               </p>
               <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" outline color="#0D0A3F" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Meetup Page</v-btn>
               &nbsp;
               <v-btn :href="chapterDetails.socialLinks[0].link" target="_blank" outline color="#0D0A3F" class="ma-0 google-font" style="border-radius:5px;text-transform: capitalize;">Facebook Page</v-btn>
                <br><br>
               <!-- <router-link to="/about" class="google-font" style="text-decoration:none;color:white">See More about {{chapterDetails.ChapterName}}</router-link> -->
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
