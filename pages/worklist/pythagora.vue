<template>
  <v-container fluid>
    <WorkCarousel :photos="photos" title="ピタゴラスイッチ" />

    <v-container fluid class="main_container">
      <WorkCard title="ドローン" name="ドローン" description="どろーん" />
    </v-container>
  </v-container>
</template>

<script>
import WorkCard from '@/components/ui/WorkCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
import WorkCarousel from '@/components/ui/WorkCarousel.vue';



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
    WorkCarousel,
  },
}
</script>