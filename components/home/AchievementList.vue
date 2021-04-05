<template>
  <div>
    <TitleBar title="活動実績" />
    <v-row>
      <v-col
      v-for="achievement in achievements"
      :key="achievement.title"
      md=6
      >
        <v-card class="mb-12" min-height="300px">
          <v-img
          src='https://cdn.vuetifyjs.com/images/carousel/bird.jpg' />
          <v-card-title v-text="achievement.title"></v-card-title>
          <v-card-text v-text="achievement.description"></v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import TitleBar from '@/components/ui/TitleBar.vue'
export default {
  components: {
    TitleBar,
  },
  data: () => ({
      achievements: [
        { title: 'アフレルスプリング2019',
        description: 'アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝アフレルスプリングカップ2019東京大会中学生ミドル部門:優勝' },
        { title: 'パ・リーグ学生ベースボールアプリ選手権',
        description: 'パ・リーグ学生ベースボールアプリ選手権:優勝' },
        { title: 'ロボカップジャパンオープン@Home simulationDSPL',
        description: 'ロボカップジャパンオープン@Home simulationDSPL 準優勝' },
      ],
  }),
}
</script>
