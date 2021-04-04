<template>
<div>
  <TitleBar title="部員の作成した作品" />
  <!-- 何故か動いた第一号 -->
  <div
  v-for="(text, i) in texts"
  :key="i">
    <WorkCard
    :title="text.title"
    :description="text.description"
    workcard="workcard"
    v-if="i%2==0"
    />
    <WorkCard
    :title="text.title"
    :description="text.description"
    v-if="i%2==1"
    />
  </div>
</div>
</template>

<script>
import WorkCard from '@/components/ui/WorkCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
export default {
  data(){
    return {
      texts: [
        {
          title: "電子工作",
          description: "電子工作班では-----------------------------------------------------------------------------------",
        },
        {
          title: "プログラミング",
          description: "プログラミング班では-----------------------------------------------------------------------------------",
        },
        {
          title: "ペットボトルロケット",
          description: "ペットボトルロケット班では-----------------------------------------------------------------------------------",
        },
        {
          title: "動画編集・Webサイト制作",
          description: "動画編集・Webサイト制作班では-----------------------------------------------------------------------------------",
        },
      ]
    }
  },
  components:{
    WorkCard,
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