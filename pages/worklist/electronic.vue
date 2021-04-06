<template>
  <v-container fluid>
    <v-carousel
      cycle
      height="600"
      :show-arrows="false"
      delimiter-icon="mdi-minus"
    >
      <v-carousel-item
        v-for="(photo, i) in photos"
        :key="i"
        :src="photo.src"
      ></v-carousel-item>
      <h1 class="carousel_title">電子工作</h1>
    </v-carousel>

    <v-container fluid class="main_container">
      <TitleBar title="1. ドローン" />
      <v-card>
        <img src='https://cdn.vuetifyjs.com/images/carousel/bird.jpg' width="100%" />
        <v-card-title>ドローン</v-card-title>
        <v-card-tex>どろーん</v-card-tex>
      </v-card>
    </v-container>
  </v-container>
</template>

<script>
import WorkCard from '@/components/ui/WorkCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';


export default {
  data () {
    return {
      photos: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
    }
  },
  components: {
    WorkCard,
    TitleBar,
  },
}
</script>

<style scoped>
  .container {
    padding:0;
  }
  .main_container {
    padding: 0 20% 0 20%;
  }
</style>