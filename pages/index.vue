<template>
  <v-app>
    <HomeCarousel />
    <v-container fluid class="main_container">
      <MainNotification />
      <AboutCard />
      <WorkList />
      <AchievementList />
    </v-container>
    <NavigationFooter />
  </v-app>
</template>

<script>
import MainNotification from '@/components/home/MainNotification.vue';
import AboutCard from '@/components/home/AboutCard.vue';
import TitleBar from '@/components/ui/TitleBar.vue';
import NavigationFooter from '@/components/layout/NavigationFooter.vue';
import WorkList from '@/components/home/WorkList.vue';
import AchievementList from '@/components/home/AchievementList.vue';



export default {
  components:{
    MainNotification,
    AboutCard,
    TitleBar,
    NavigationFooter,
    WorkList,
    AchievementList,
  }
}
</script>

<style>
 .container {
   padding: 0;
 }
  .main_container {
    padding: 0 20% 0 20%;
  }
</style>