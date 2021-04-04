<template>
  <v-carousel
  class="mb-16"
  hide-delimiters
  :show-arrows="false"
  cycle
  height="300">
    <v-carousel-item
      v-for="(photo,i) in photos"
      :key="i"
      :src="photo.src"
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
  export default {
    data() {
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
    }
  }
</script>
