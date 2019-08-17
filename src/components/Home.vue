<template>
  <v-container grid-list-md>
    <v-layout align-center justify-center row fill-height class="text-center">
      <v-flex align-self-center class="text-sm-right">
        <v-btn large router to="/meetups" class="primary">Explore Meetups</v-btn>
      </v-flex>
      <v-flex xs12 sm6 class="text-xs-center text-sm-left">
        <v-btn large router to="/meetups" class="primary">Organize Meetup</v-btn>
      </v-flex>
    </v-layout>
    <v-layout>
      <v-carousel :show-arrows="false">
        <v-carousel-item
        v-for="meetup in meetups"
        :key="meetup.id"
        :src="meetup.imageUrl">
        <div class="title">
          {{meetup.title}}
        </div>
        </v-carousel-item>
      </v-carousel>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      meetups: [
        { imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/dc/Skyscrapers_of_Shinjuku_2009_January_%28revised%29.jpg', id: 'TEST', title: 'TEST MEETUP' },
        { imageUrl: 'https://www.thebalancecareers.com/thmb/7RNbnMgqp7sHt5i7kAwvwtNKbG4=/3865x2576/filters:no_upscale():max_bytes(150000):strip_icc()/high-angle-view-of-lower-east-side-manhattan-downtown--new-york-city--usa-640006562-5ae52a273de423003776ae2e.jpg', id: 'TEST2', title: 'OTHER TEST' }
      ]
    }
  }
}
</script>

<style scoped>
  .title {
    text-align: center;
    color: black;
    padding-top: 1em;
    padding-bottom: 1em;
    background-color: #fbf7f3;
    opacity: 0.6;
  }
</style>
