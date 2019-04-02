<template>
  <div class="slide-con" :class="{mobile:$q.platform.is.mobile}">
    <slider animation="fade" :controlBtn="false" height="100%" :autoplay="true" :interval="4000">
      <slider-item>
        <div class="img-bg img-bg1 column justify-center items-center">
          <h6 class="title">"我们更专业"</h6>
          <h1 class="big-title"><span class="theme-color">企业级</span>软件开发服务商</h1>
          <p class="normal-title">为企业提供高端软件定制和互联网解决方案服务</p>
        </div>
      </slider-item>
      <slider-item>
        <div class="img-bg img-bg2 column justify-center items-center">
          <h6 class="title">"我们更全能"</h6>
          <h1 class="big-title"><span class="theme-color">多平台</span>系统解决方案专家</h1>
          <p class="normal-title">积聚三十多个主流行业，上千个全方案解决实践，只为更好的为您服务</p>
        </div>
      </slider-item>
      <slider-item>
        <div class="img-bg img-bg3 column justify-center items-center">
          <h6 class="title">"我们更稳定"</h6>
          <h1 class="big-title">高性能业务支撑<span class="theme-color">安全稳定</span></h1>
          <p class="normal-title">以先进的技术，产品与服务，为企业提供专业的电商平台系统搭建</p>
        </div>
      </slider-item>
    </slider>
  </div>
</template>

<script>
export default {
  name: 'MySlider',
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
    height 80vh
    color #fff
    width 100%
    text-align center
    .img-bg1
      background url('~assets/images/homeb1.jpg')
    .img-bg2
      background url('~assets/images/homeb2.jpg')
    .img-bg3
      background url('~assets/images/homeb3.jpg')
    .img-bg
      width 100%
      height 100%
      background-size cover
      background-position center center

      .normal-title
        font-size 1rem
      .big-title
        font-size 3.75rem
        font-weight 500
        margin-bottom .9375rem
        margin-top 0
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
  .slide-con.mobile
    height 100vh
</style>
