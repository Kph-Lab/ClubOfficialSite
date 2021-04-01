<template>
<v-app>
  <HomeCarousel />
  <MainNotification />
  <TitleBar title="活動概要" />
  <AboutCard />
  <TitleBar title="部員の作成した作品" />
  <WordList />
  <TitleBar title="活動実績" />
  <NavigationFooter />

</v-app>
</template>

<script>
import MainNotification from '@/components/home/MainNotification.vue';
import AboutCard from '@/components/home/AboutCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
import NavigationFooter from '@/components/layout/NavigationFooter.vue';
import WordList from '@/components/home/WordList.vue';



export default {
  components:{
    MainNotification,
    AboutCard,
    TitleBar,
    NavigationFooter,
    WordList,
  }
}
</script>
