<template>
<v-app>
  <HomeCarousel />
  <MainNotification />
  <TitleBar title="活動概要" />
  <About />
  <TitleBar title="部員の作成した作品" />
  <TitleBar title="活動実績" />
  <NavigationFooter />

</v-app>
</template>

<script>
import MainNotification from '@/components/home/MainNotification.vue';
import About from '@/components/home/About.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
import NavigationFooter from '@/components/layout/NavigationFooter.vue';



export default {
  components:{
    MainNotification,
    About,
    TitleBar,
    NavigationFooter,
  }
}
</script>
