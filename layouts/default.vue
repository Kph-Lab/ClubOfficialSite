<template>
  <v-app>
    <nuxt />
    <NavigationFooter />
  </v-app>
</template>

<style>
  .col {
    padding-top: 0;
    padding-bottom: 0;
  }
</style>

<script>
import NavigationFooter from '@/components/layout/NavigationFooter.vue';
export default {
  components: {
    NavigationFooter,
  },
}
</script>
