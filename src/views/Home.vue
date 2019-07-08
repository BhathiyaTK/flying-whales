<template>
  <v-content class="pa-0">

    <v-container fluid class="my-4">
      <v-layout wrap align-center justify-center row fill-height class="">
        <v-flex xs12 md10 >
          <HomeStartScreen />
        </v-flex>
      </v-layout>
    </v-container>

     <v-container fluid style="background-color:#F9F9F9" >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <AboutSEF />
        </v-flex>
      </v-layout>
    </v-container>

    <!-- <v-container fluid style="background-color:#F9F9F9" >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <whatWeDo />
        </v-flex>
      </v-layout>
    </v-container> -->

    <v-container fluid style="background-color:#F9564D" >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <Mission />
        </v-flex>
      </v-layout>
    </v-container>

    <!-- <v-container fluid >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <eventshowcase />
        </v-flex>
      </v-layout>
    </v-container> -->
  
    <v-container fluid class="py-5" style="background-color:#F9F9F9">
      <v-layout wrap align-start justify-start row fill-height>
        <v-flex xs12 sm10 md10 offset-sm1 offset-md1 offset-lg1 >
          <p class="google-font mb-2" style="font-size:150%">Testimonials from our guest speakers</p>
        </v-flex>
        <v-flex xs12 sm10 md10 offset-sm1 offset-md1 offset-lg1 >
          <v-layout wrap  row fill-height>
            <v-flex v-for="item in sefDetails.testimonials" v-bind:key="item.id" xs12 md4>
              <Testimonial v-bind:name=item.name v-bind:bio=item.bio v-bind:content=item.content v-bind:imgSrc=item.imgSrc />
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
    
     <!-- <v-container fluid >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
          <wtmInfo />
        </v-flex>
      </v-layout>
    </v-container> -->

    <v-container fluid >
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10>
          <partners />
        </v-flex>
      </v-layout>
    </v-container>

    


  </v-content>
  
</template>

<script>
  import HomeStartScreen from '@/components/home/HomeStartScreen'
  import whatWeDo from '@/components/home/whatWeDo'
  import AboutGDGChapter from '@/components/home/AboutGDGChapter'
  import AboutSEF from '@/components/home/AboutSEF'
  import Mission from '@/components/home/Mission'
  import eventshowcase from '@/components/home/eventshowcase'
  // import wtmInfo from '@/components/home/wtmInfo'
  import partners from '@/components/home/partners'
  // import featureEvent from '@/components/home/featureEvent'
  import Testimonial from '@/components/home/Testimonial'

  import SEFDetails from '@/assets/data/sefHomePage.json'
  
  export default {
    components: {
      HomeStartScreen,
      // whatWeDo,
      // AboutGDGChapter,
      Mission,
      AboutSEF,
      eventshowcase,
      // wtmInfo,
      partners,
      // featureEvent
      Testimonial
    },
      data() {
        return {
             sefDetails : SEFDetails
        }
    },
  }
</script>
