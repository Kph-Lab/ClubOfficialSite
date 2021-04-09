<template>
  <div>
    <TitleBar :title="title" />
    <v-card>
      <img
      src='https://cdn.vuetifyjs.com/images/carousel/bird.jpg'
      width="100%"
      />
      <v-card-title>{{ name }}</v-card-title>
      <v-card-text>{{ description }}</v-card-text>
    </v-card>
  </div>
</template>

<script>
import TitleBar from '@/components/ui/TitleBar.vue';

export default{
  components: {
    TitleBar,
  },
  props: [
    "title",
    "description",
    "name",
  ],
}
</script>
