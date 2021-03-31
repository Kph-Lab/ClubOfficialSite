<template>
  <v-banner
  elevation="3"
  max-width="70%"
  min-width="70%"
  class="mx-auto">{{ title }}</v-banner>
</template>

<script>
export default{
  props: [
    "title",
  ]
}
</script>
