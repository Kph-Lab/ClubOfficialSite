<template>
<div>
    <TitleBar title="活動概要" />
    <v-card
      class="mx-auto mb-16"
    >
      <v-row v-bind:class="[
      isActive === true ? 'active' : 'inactive'
      ]">
        <v-col class="py-0" md=4>
          <v-img
            src='https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg'
            height="250px"
          ></v-img>
        </v-col>
        <v-col class="py-0" md=8>

          <v-card-text>
            物理部ではうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたらうんたらかんたら
          </v-card-text>
        </v-col>
      </v-row>
    </v-card>
</div>
</template>

<script>
import TitleBar from '@/components/ui/TitleBar.vue';

export default {
  components:{
    TitleBar,
  },
  data: function() {
    return {
      isActive: false
    }
  }
}
</script>
