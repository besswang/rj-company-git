<template>
  <div class="slide-con">
    <slider animation="fade" :controlBtn="false" height="100%" :autoplay="false">
      <slider-item>
        <div class="img-bg1">
          <h6 class="title">"我们更专业"</h6>
          <h1 class="big-title"><span class="theme-color">企业级</span>软件开发服务商</h1>
          <p class="normal-title">为企业提供高端软件定制和互联网解决方案服务</p>
        </div>
      </slider-item>
      <slider-item></slider-item>
    </slider>
  </div>
</template>

<script>
export default {
  // name: 'Slider',
  data () {
    return {

    }
  },
  methods: {
    hello ($event) {
      console.log(`hello index: ${$event}`)
    }
  }
}
</script>

<style lang="stylus">
@import '~variables'
  .slide-con
    height 884px
    color #fff
    width 100%
    text-align center
    .img-bg1
      width 100%
      height 100%
      background url('~assets/images/homeb1.jpg')
      .normal-title
        font-size 1rem
      .big-title
        font-size 3.75rem
        font-weight 500
        margin-bottom .9375rem
      .title
        margin-top 0
        font-size 1.125rem
        position relative
        &::after
          content ' '
          position absolute
          bottom -.5rem
          left 50%
          margin-left -2.1875rem
          width 4.375rem
          height .25rem
          background $orange
      .theme-color
        color $orange

</style>
