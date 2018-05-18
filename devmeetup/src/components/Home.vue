<template>
  <v-container>
    <v-layout row wrap>
      <v-flex xs12 sm6 class="text-xs-center text-sm-right">
        <v-btn large router to="/meetups" class="info">Explore Meetups</v-btn>
      </v-flex>
      <v-flex xs12 sm6 class="text-xs-center text-sm-left">
        <v-btn large router to="/meetups/register" class="info">Register A Meetup</v-btn>
      </v-flex>
    </v-layout>
    <v-layout row wrap class="mt-2">
      <v-flex xs12>
          <v-carousel>
            <v-carousel-item
              v-for="meetup in meetups"
              :src="meetup.imageUrl"
              :key="meetup.id">
              <div class="title">
                {{ meetup.title }}
              </div>
            </v-carousel-item>
          </v-carousel>
      </v-flex>
    </v-layout>
    <v-layout row wrap class="mt-2">
      <v-flex xs12 class="text-xs-center">
        <p>Join our meetups!</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        meetups: [
          {
            imageUrl: 'https://images.businessoffashion.com/site/uploads/2018/02/shutterstock_111362132.jpg',
            id: 'sdfsf',
            title: 'Meetup in Paris'
          },
          {
            imageUrl: 'https://www.lonelyplanet.com/travel-blog/tip-article/wordpress_uploads/2017/08/shutterstock_611229743-bde2e023e33c.jpg',
            id: 'dsfsfsdf',
            title: 'Meetup in Switzerland :)'
          }
        ]
      }
    }
  }
</script>

<style scoped>
.title {
  position: absolute;
  bottom: 50px;
  background-color: rgba(0, 0, 0, .5);
  color: white;
  font-size: 2em;
  padding: 10px;
  left: 50%;
  transform: translateX(-50%);
}
</style>