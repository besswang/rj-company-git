<template>
  <q-page class="flex flex-center">
    <my-slider />
    <div class="q-pa-md row q-col-gutter-x-md wrap">
      <div class="col-sm-6 col-md-3" v-for="(list, index) in carditem" :key="index">
        <q-card
        class="my-card text-white"
        :class="`cbg${index}`"
        >
          <h5 v-text="list.title"></h5>
          <p v-text="list.info"></p>
        </q-card>
      </div>
    </div>
  </q-page>
</template>
<script>
import MySlider from '../components/MySlider.vue'
export default {
  name: 'Home',
  components: {
    MySlider
  },
  data () {
    return {
      carditem: [
        {
          title: '手机APP',
          info: '移动WEB、APP H5动画、小程序'
        }, {
          title: '手机APP',
          info: '移动WEB、APP H5动画、小程序'
        }, {
          title: '手机APP',
          info: '移动WEB、APP H5动画、小程序'
        }, {
          title: '手机APP',
          info: '移动WEB、APP H5动画、小程序'
        }

      ],
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
    }
  },
  method: {

  }
}
</script>
<style lang="stylus" scoped>
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
</style>
