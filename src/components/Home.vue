<template>
  <v-container>
    <v-layout row wrap class="mb-2">
      <v-flex xs12 sm6 class="text-xs-center text-sm-right">
        <v-btn large router to="/meetups" class="info">Explore Meetups</v-btn>
      </v-flex>
      <v-flex xs12 sm6 class="text-xs-center text-sm-left">
        <v-btn large router to="/meetup/new" class="info">Organize Meetups</v-btn>
      </v-flex>
    </v-layout>
    <v-layout>
      <v-flex xs12>
          <v-carousel>
            <v-carousel-item v-for="meetup in meetups" v-bind:src="meetup.imageUrl" :key="meetup.id">
              <div class="title"> {{ meetup.title }}</div>
            </v-carousel-item>
          </v-carousel>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        meetups: [
          { imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/8/8d/New_York_NYC.jpg', id: 'kjakdj23kj', title: 'Meetup in NY' },
          { imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/8/8a/Paris_vue_d%27ensemble_tour_Eiffel.jpg', id: 'kjakdj23k22j', title: 'Meetup in Paris' }
        ]
      }
    }
  }
</script>

<style scoped>
  .title{
    position: absolute;
    bottom: 50px;
    background-color: rgba( 0, 0, 0, 0.5);
    color: white;
    font-size: 2em;
    padding: 30px;
  }
</style>
