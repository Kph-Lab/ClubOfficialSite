<template>
  <v-banner
  elevation="3"
  max-width="60%"
  class="mx-auto mb-8"
  :styles="{ }"
  >{{ title }}</v-banner>
</template>

<script>
export default{
  props: [
    "title",
  ]
}
</script>
