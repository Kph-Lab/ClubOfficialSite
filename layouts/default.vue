<template>
  <v-app>
    <nuxt />
    <NavigationFooter />
  </v-app>
</template>

<script>
import NavigationFooter from '@/components/layout/NavigationFooter.vue';
export default {
  components: {
    NavigationFooter,
  },
}
</script>

<style>
  .col {
    padding-top: 0;
    padding-bottom: 0;
  }
  .container {
    padding: 0;
  }
  .main_container {
    padding: 0 20% 0 20%;
  }
</style>
