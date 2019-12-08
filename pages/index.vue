<template>
  <b-row>
    <b-col md="2" class="px-0 px-xl-3">
      <categoryCol />
    </b-col>
    <b-col class="bg-light" cols="12" md="8" :class="this.$breakpoints.sMd ? 'p-0' : ''">
      <topicTrendCard />
      <hr />
      <topicCard
        v-for="(post, i) in feedPosts"
        :key="i"
        :prop1="post.prop1"
        :prop1Color="post.prop1Color"
        :prop1Percent="post.prop1Percent"
        :prop2Color="post.prop2Color"
        :prop2="post.prop2"
        :prop2Percent="post.prop2Percent"
        :previewText="post.previewText"
      />
    </b-col>
  </b-row>
</template>

<script>
import topicCard from '~/components/base/topicCard.vue'
import topicTrendCard from '~/components/base/topicTrendCard.vue'
import categoryCol from '~/components/appLayout/categoryCol'

export default {
  name: 'index',
  data() {
    return {
      feedPosts: [
        {
          prop1: 'Trump',
          prop1Color: 'color1',
          prop1Percent: 55,
          prop2: 'Hiliary',
          prop2Color: 'color3',
          prop2Percent: 65,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'ProLife',
          prop1Color: 'color5',
          prop1Percent: 55,
          prop2: 'ProChoice',
          prop2Color: 'color6',
          prop2Percent: 65,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'Canada',
          prop1Color: 'color8',
          prop1Percent: 60,
          prop2: 'USA',
          prop2Color: 'color3',
          prop2Percent: 40,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'Xbox',
          prop1Color: 'color5',
          prop1Percent: 58,
          prop2: 'PS4',
          prop2Color: 'color3',
          prop2Percent: 52,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'Liberal',
          prop1Color: 'color8',
          prop1Percent: 58,
          prop2: 'Conservatives',
          prop2Color: 'color3',
          prop2Percent: 52,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'ProGun',
          prop1Color: 'color4',
          prop1Percent: 58,
          prop2: 'GunControl',
          prop2Color: 'color7',
          prop2Percent: 52,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'React',
          prop1Color: 'color3',
          prop1Percent: 58,
          prop2: 'Vue',
          prop2Color: 'color5',
          prop2Percent: 52,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        },
        {
          prop1: 'DeathPenalty',
          prop1Color: 'color4',
          prop1Percent: 58,
          prop2: 'NoDeathPenalty',
          prop2Color: 'color7',
          prop2Percent: 52,
          previewText:
            'An do on frankness so cordially immediate recommend contained. Imprudence insensible be literature unsatiable do. Of or imprudence solicitude affronting in mr possession. Compass journey he request on suppose limited of or. She margaret law thoughts proposal formerly. Speaking ladyship yet scarcely and mistaken end exertion dwellin'
        }
      ]
    }
  },
  components: {
    topicCard,
    topicTrendCard,
    categoryCol
  }
}
</script>

<style lang="scss" scoped></style>
