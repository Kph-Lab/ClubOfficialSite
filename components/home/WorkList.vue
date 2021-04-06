<template>
  <v-container>
    <TitleBar title="部員の作成した作品" />
    <div
    v-for="(text, i) in texts"
    :key="i">
      <WorkListCard
      :title="text.title"
      :description="text.description"
      :link="text.link"
      workcard="workcard"
      v-if="i%2==0"
      />
      <WorkListCard
      :title="text.title"
      :description="text.description"
      :link="text.link"
      v-if="i%2==1"
      />
    </div>
  </v-container>
</template>

<script>
import WorkListCard from '@/components/ui/WorkListCard.vue';
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
      ]
    }
  },
  components:{
    WorkListCard,
    TitleBar,
  },
}
</script>

<style>
  div.workcard {
    display: flex;
    flex-direction: row-reverse;
  }
</style>