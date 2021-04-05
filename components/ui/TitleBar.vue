<template>
  <v-banner
  elevation="4"
  class="mx-auto mb-8"
  >{{ title }}</v-banner>
</template>

<script>
export default{
  props: [
    "title",
  ]
}
</script>

<style>
  .v-banner {
    border-left: 10px solid black !important;
  }
</style>