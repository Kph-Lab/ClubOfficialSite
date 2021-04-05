<template>
    <v-card
      class="mx-auto mb-12"
    >
      <v-row :class="{ workcard }">
        <v-col class="py-0" md=4>
          <v-img
            src='https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
            height="250px" />
        </v-col>
        <v-col class="px-8" md=8>
          <v-card-title>{{ title }}</v-card-title>
          <v-card-text>{{ description }}</v-card-text>
        </v-col>
      </v-row>
    </v-card>
</template>

<script>
export default{
  props: [
    "title",
    "description",
    "workcard",
  ]
}
</script>
