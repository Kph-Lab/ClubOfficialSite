<template>
<v-app>
  <v-carousel hide-delimiters :show-arrows="false" cycle height="300">
    <v-carousel-item
      v-for="(item,i) in photos"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
  <v-card
    class="mx-auto"
    max-width="70%"
  >
    <v-row>
      <v-col md=5>
        <v-img
          src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
          width="100%" height="100%"
        ></v-img>
      </v-col>
      <v-col md=7>
        <v-card-title>
          文化祭の特設ページを開設しました‼‼
        </v-card-title>

        <v-card-text>
          2021年度の文化祭の特設ページを開設しました。物理部の紹介動画や、部員の作成した作品・それについての部誌を閲覧できます(適当)。
        </v-card-text>
      </v-col>
    </v-row>
  </v-card>
  <v-banner
  elevation="3"
  min-width="70%"
  class="mx-auto">活動概要</v-banner>
  <v-card
    class="mx-auto"
    max-width="70%"
  >
    <v-row>
      <v-col md=4>
        <v-img
          src='https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
          height="300px"
        ></v-img>
      </v-col>
      <v-col md=8>

        <v-card-text>
          物理部ではうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたら
        </v-card-text>
      </v-col>
    </v-row>
  </v-card>
  <v-banner
  elevation="3"
  min-width="70%"
  class="mx-auto">部員の作成した作品</v-banner>
  <v-banner
  elevation="3"
  min-width="70%"
  class="mx-auto">活動実績</v-banner>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</v-app>
</template>

<script>
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
  }
</script>