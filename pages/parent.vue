<template>
  <div class="Parent">
    <h2 class="Parent-Heading">
      臨時休校中の新型コロナウイルス感染症対応についてのお願い
    </h2>
    <div v-for="(item, i) in items" :key="i">
      <TextCard :title="item.title" :body="item.body" />
    </div>
  </div>
</template>
<script lang="ts">
import TextCard from '@/components/TextCard.vue'
export default {
  components: {
    TextCard
  },
  data() {
    return {
      items: [
        {
          title: '1 感染予防・健康管理',
          body:
            '〇　不特定多数の人の集まる場所等への外出を避け、基本的に自宅で過ごしてください。<br />〇　手洗い、咳エチケット等により、感染予防に努めてください。<br />　<a href="https://www.city.fukuoka.lg.jp/data/open/cnt/3/72498/1/nCoV_flyer_200228.pdf?20200312113320" target="_blank" rel="noopener">【参考】感染予防のポイント</a> <br />〇　規則正しい生活を心がけ、日常の健康管理に十分気を付けてください。'
        },
        {
          title: '2 感染症を疑う場合の対応',
          body:
            '〇　風邪の症状や、37.5度以上の発熱が４日以上続いている、強いだるさ（倦怠感）、息苦しさ（呼吸困難）がある場合は、各保健所にご相談ください。<br />〇  「新型コロナウイルス感染症にかかる相談窓口について」（福岡市）<br /><a href="https://www.city.fukuoka.lg.jp/hofuku/hokenyobo/health/kansen/nCorV.html#te" target="_blank" rel="noopener">https://www.city.fukuoka.lg.jp/hofuku/hokenyobo/health/kansen/nCorV.html#te</a>'
        },
        {
          title: '3 その他',
          body: '〇　市立学校における臨時休業等の実施<br /><a href="https://www.city.fukuoka.lg.jp/hofuku/hokenyobo/health/kansen/nCorV.html#sh" target="_blank" rel="noopener">https://www.city.fukuoka.lg.jp/hofuku/hokenyobo/health/kansen/nCorV.html#sh</a>'
        }
      ]
    }
  },
  head() {
    return {
      title: 'お子様をお持ちの皆様へ'
    }
  }
}
</script>
<style lang="scss">
.Parent {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
}
a {
  @include text-link();
}
</style>
