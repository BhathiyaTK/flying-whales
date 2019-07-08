<template>
    <v-container class="pa-2 my-0">
        <v-layout wrap align-center justify-center row fill-height class="mt-4 elevation-2 white" style="border:1px solid #e0e0e0;border-radius:5px;">
            <v-flex xs12  class="pt-5" >
                <v-layout align-center justify-center>
                     <v-avatar min-height="400px" size="15vh">
                        <v-img
                            :src="require(`@/assets/img_/testimonial/${imgSrc}`)"
                            :lazy-src="require(`@/assets/img_/testimonial/${imgSrc}`)"
                            >
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
                    </v-avatar>
                </v-layout>
            </v-flex>
           <v-flex xs12  class="pa-2 py-4 px-3 justify-center"  >
                <p class="google-font mb-0 text-xs-center" style="font-size:150%;color:rgb(43, 206, 137)">{{name}}</p>
                <p class="google-font mb-3 text-xs-center" style="font-size:100%;color:#454545">{{bio}}</p>
                <!-- <span class="google-font mt-1 mb-0 grey--text"  style="font-size:105%">
                    <v-icon small>insert_invitation</v-icon>
                    {{eventDetails.EventDate.Date +'/'+ eventDetails.EventDate.Month +'/'+ eventDetails.EventDate.Year}} 
                    &nbsp;
                    <v-icon small>watch_later</v-icon>
                    {{eventDetails.EventTime.StartTime +' - '+ eventDetails.EventTime.EndTime}}
                    &nbsp;
                    <v-icon small>map</v-icon>
                    {{eventDetails.EventVenue | summery(50)}} <a :href="eventDetails.EventVenueMapLink" target="_blank">(Map)</a>
                </span>     -->
               <p class="google-font mt-2 mb-1 text-xs-center" style="font-size:120%;color:#757575">
                   {{content}}
               </p>
                
                <!-- <v-btn color="#1a73e8" v-if="eventDetails.RegistrationLink.length>0" :href="eventDetails.RegistrationLink" target="_blank" class="ma-0 elevation-0 my-2" dark style="text-transform: capitalize;border-radius:5px;"> 
                    Registration Link
                </v-btn>
                &nbsp;

                <v-tooltip top slot="activator" v-if="eventDetails.EventWebsite.length>0">
                    <v-btn flat icon color="#616161" class="ma-0 elevation-0" slot="activator" 
                    :href="eventDetails.EventWebsite"
                    target="_blank"
                    style="text-transform: capitalize;border-radius:5px;"> 
                        <v-icon>language</v-icon>
                    </v-btn>
                    <span>See {{eventDetails.FeatureEventName}} Website</span>
                </v-tooltip>

                <v-tooltip top slot="activator" 
                v-if="eventDetails.MeetupLink.length>0">
                    <v-btn flat icon color="#616161"
                    :href="eventDetails.MeetupLink"
                    target="_blank"
                    class="ma-0 elevation-0" slot="activator" style="text-transform: capitalize;border-radius:5px;"> 
                        <v-icon>fab fa-meetup</v-icon>
                    </v-btn>
                    <span>See {{eventDetails.FeatureEventName}} Meetup</span>
                </v-tooltip>

                <v-tooltip top slot="activator" v-if="eventDetails.FBEventPageURL.length>0">
                    <v-btn flat icon color="#616161"
                    :href="eventDetails.FBEventPageURL"
                    target="_blank"
                    class="ma-0 elevation-0" slot="activator" style="text-transform: capitalize;border-radius:5px;"> 
                        <v-icon >fab fa-facebook-f</v-icon>
                    </v-btn>
                    <span>See {{eventDetails.FeatureEventName}} Facebook Page</span>
                </v-tooltip> -->
            
            </v-flex> 
        </v-layout>

    </v-container>
</template>

<script>
import eventDetails from '@/assets/data/featureEvent.json'
export default {
    props : ['name', 'bio', 'content','imgSrc'],
    components:{
    },
    data() {
        return {
            eventDetails:eventDetails
        }
    },
    created(){
        
    },
    methods:{
        getImgUrl(pic) {
            if(pic.length>0){
                return require('@/assets/img/featureEvent/'+pic)
            }else{
                return require('@/assets/img/featureEvent/imagenotfound.png')
            }
        },
    },
    filters:{
        summery: (val,num)=>{
            return val.substring(0,num)+".."
        },
        dateFilter: (value)=>{
            const date = new Date(value)
            return date.toLocaleString(['en-US'], {month: 'short', day: '2-digit', year: 'numeric'})
        }
    }
}
</script>
