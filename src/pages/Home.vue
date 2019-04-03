<template>
  <q-page class="flex flex-center">
    <my-slider />
    <div class="q-pa-md row q-col-gutter-xl text-center card-row">
      <div class="col-xs-6 col-sm-6 col-md-3 card-col" v-for="(list, index) in cardList" :key="index">
        <q-card
        class="my-card text-white"
        :class="`cbg${index}`"
        >
          <h6 v-text="list.title"></h6>
          <p v-text="list.info"></p>
        </q-card>
      </div>
    </div>
  </q-page>
</template>
<script>
import MySlider from '../components/MySlider.vue'
import { CARD_LIST } from '../meta/meta.js'
export default {
  name: 'Home',
  components: {
    MySlider
  },
  data () {
    return {
      cardList: CARD_LIST
    }
  }
}
</script>
<style lang="stylus" scoped>
.card-row
  width 68.75rem
  .card-col
    padding .3125rem
    .cbg0
      background url('~assets/images/cbg0.jpg')
    .cbg1
      background url('~assets/images/cbg1.jpg')
    .cbg2
      background url('~assets/images/cbg2.jpg')
    .cbg3
      background url('~assets/images/cbg3.jpg')
    .my-card
      background-position center center
      background-size cover
      background-repeat no-repeat
      padding 2.5rem
      height 25rem
      @media screen and (max-width 700px)
        height 12.5rem
      h6
        padding-bottom 1.875rem
      p
        font-size .875rem
        max-width 6.875rem
        margin 0 auto
</style>
