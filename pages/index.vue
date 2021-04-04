<template>
  <v-app>
    <HomeCarousel />
    <MainNotification />
    <AboutCard />
    <WorkList />
    <TitleBar title="活動実績" />
    <NavigationFooter />
  </v-app>
</template>

<script>
import MainNotification from '@/components/home/MainNotification.vue';
import AboutCard from '@/components/home/AboutCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
import NavigationFooter from '@/components/layout/NavigationFooter.vue';
import WorkList from '@/components/home/WorkList.vue';



export default {
  components:{
    MainNotification,
    AboutCard,
    TitleBar,
    NavigationFooter,
    WorkList,
  }
}
</script>
