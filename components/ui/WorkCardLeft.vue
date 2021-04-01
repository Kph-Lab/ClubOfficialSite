<template>
    <v-card
      max-width="70%"
      class="mx-auto"
    >
      <v-row class="workcard">
        <v-col md=4>
          <v-img
            src='https://cdn.vuetifyjs.com/images/carousel/sky.jpg'
            height="300px" />
        </v-col>
        <v-col md=8>
          <v-card-title>{{ title }}</v-card-title>
          <v-card-text>
            物理部ではうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたら
          </v-card-text>
        </v-col>
      </v-row>
    </v-card>
</template>

<script>
export default{
  props: [
    "title",
  ]
}
</script>
