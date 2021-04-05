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
    <h1 class="carousel_title">Kaijo Physics Club</h1>
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

<style>
.carousel_title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateY(-50%) translateX(-50%);
  color: white;
  font-size: 60px;
}
</style>