<template>
  <div>
    <TitleBar title="部員の作成した作品" />
    <div v-for="(text, i) in texts" :key="i">
      <v-card
        class="mx-auto mb-12"
      >
        <v-row v-bind:class="[
        i % 2 == 0 ? '' : 'reverse'
        ]">
          <v-col class="py-0" md=4>
            <v-img
              src='https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
              height="250px" />
          </v-col>
          <v-col class="px-8" md=8>
            <v-card-title>{{ text.title }}</v-card-title>
            <v-card-text>{{ text.description }}</v-card-text>
            <v-btn
              nuxt
              color="cyan darken-1"
              outlined
              :to="text.link"
            >
              作品を見る
            </v-btn>
          </v-col>
        </v-row>
      </v-card>
    </div>
  </div>
</template>

<script>
import TitleBar from '@/components/ui/TitleBar.vue';

export default {
  data(){
    return {
      texts: [
        {
          title: "電子工作",
          description: "電子工作班では-----------------------------------------------------------------------------------",
          link: "/worklist/electronic",
        },
        {
          title: "プログラミング",
          description: "プログラミング班では-----------------------------------------------------------------------------------",
          link: "/worklist/programming",
        },
        {
          title: "ペットボトルロケット",
          description: "ペットボトルロケット班では-----------------------------------------------------------------------------------",
          link: "/worklist/bottlerocket",
        },
        {
          title: "動画編集・Webサイト制作",
          description: "動画編集・Webサイト制作班では-----------------------------------------------------------------------------------",
          link: "/worklist/lectureship",
        },
        {
          title: "ピタゴラスイッチ",
          description: "動画編集・Webサイト制作班では-----------------------------------------------------------------------------------",
          link: "/worklist/pythagora",
        },
      ],
    }
  },
  components: {
    TitleBar,
  },
}
</script>

<style>
  div.reverse {
    display: flex;
    flex-direction: row-reverse;
  }
</style>