<template>
  <div>
    <HomeCarousel />
    <v-container fluid class="main_container">
      <MainNotification />
      <AboutCard />
      <WorksList />
      <AchievementList />
    </v-container>
  </div>
</template>

<script>
import MainNotification from '@/components/home/MainNotification.vue';
import AboutCard from '@/components/home/AboutCard.vue';
import AchievementList from '@/components/home/AchievementList.vue';
import WorksList from '@/components/home/WorksList.vue';

export default {
  components:{
    MainNotification,
    AboutCard,
    AchievementList,
    WorksList,
  }
}
</script>
