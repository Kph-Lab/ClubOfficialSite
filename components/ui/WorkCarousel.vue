<template>
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
    <h1 class="carousel_title">{{ title }}</h1>
  </v-carousel>
</template>

<script>

export default {
  props: [
    "photos",
    "title",
  ]
}
</script>
