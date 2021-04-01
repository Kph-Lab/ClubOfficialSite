<template>
<div>
  <div
  v-for="(text, i) in texts"
  :key="i">
    <WorkCardRight
    :title="text.title"
    :description="text.description"
    v-if="i%2==0"
    />
    <WorkCardLeft
    :title="text.title"
    :description="text.description"
    v-if="i%2==1"
    />
  </div>
</div>
</template>

<script>
import WorkCardLeft from '@/components/ui/WorkCardLeft.vue';
import WorkCardRight from '@/components/ui/WorkCardRight.vue';
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
    WorkCardRight,
    WorkCardLeft,
  },
}
</script>

<style>
  div.workcard:nth-of-type(odd) {
    display: flex;
    flex-direction: row-reverse;
  }
</style>