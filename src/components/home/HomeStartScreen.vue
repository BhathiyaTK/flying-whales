<template>
    <v-container class="pa-0">
        <v-layout wrap align-center justify-center row fill-height >
           <v-flex xs12 sm5 md3 lg3 xl3 class="text-xs-center pa-3">
                <v-img class="center center"
                    :src="require('@/assets/img_/brand/sefLogo.png')"
                    :lazy-src="require('@/assets/img_/brand/sefLogo.png')"
                    width="100%">
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
            <v-flex xs12 sm7 md8 lg8 xl8 class="">
                <!-- <p class="google-font mb-1" style="font-weight: 350;color: #616161;font-size:300%"><b>Make good things 
                    <span style="color: #1a73e8;">together</span>.</b>
                </p> -->
                <p class="google-font mb-1" style="font-weight: 350;color: #0D0A3F;font-size:300%"><b>
                    <span style="color: #0D0A3F;">Sustainable</span>  </b><br>
                    Education Foundation 
                </p>
                <!-- <p class="google-font mt-0" style="font-size:180%">{{chapterDetails.ChapterName}}</p> -->
                <p class="google-font" style="font-size:110%">{{sefDetails.shortDescription}}</p>
                <p class="google-font" style="font-size:110%;color:#9e9e9e">
                    <!-- <span v-for="(item,i) in chapterDetails.ChapterHashTags" :key="i">
                        #{{item}} &nbsp;
                    </span> -->
                </p>

                <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" class="ma-0 google-font elevation-1" color="#0D0A3F" style="text-transform: capitalize;border-radius:5px;color:white; font-weight : bold">LEARN ABOUT US</v-btn>

                &nbsp;

                <v-btn :href="chapterDetails.ChapterMeetupLink" target="_blank" class="ma-0 google-font elevation-1" color="cyan" style="text-transform: capitalize;border-radius:5px;color:white;font-weight : bold">EVENTS</v-btn>

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
