<template>
  <div class="footer-con q-pa-md">
    <div class="row q-col-gutter-x-md wrap">
      <div class="col-sm-6 col-md-3">
        <p class="footer-title">站点导航</p>
        <ul>
          <li>首页</li>
          <li>服务</li>
          <li>案例</li>
          <li>观点</li>
          <li>关于</li>
        </ul>
      </div>
      <div class="col-sm-6 col-md-3">
        <p class="footer-title">联系我们</p>
        <ul>
          <li>张经理 187-0987-4765</li>
          <li>李经理 187-0987-4765</li>
          <li>座机 0571-88542038</li>
          <li>商务合作 mingaskshdhf@163.com</li>
          <li>杭州市余杭区西溪八方城9楼403室</li>
        </ul>
      </div>
      <div class="col-sm-6 col-md-3">
        <p class="footer-title">工作时间</p>
        <ul>
          <li>周一至周五</li>
          <li>09:00 - 18:00 （GMT+8）</li>
        </ul>
      </div>
      <div class="col-sm-6 col-md-3">
        <p class="footer-title">官方微信</p>
        <ul>
          <li>
            <img class="code" src="~assets/images/code.jpg" alt="">
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<style lang="stylus">
  .footer-con
    background #2e2e2e
    color #999
    padding 1.875rem 28%
    .footer-title
      font-size 1.125rem
      color #ccc
    ul
      font-size .75rem
      li
        padding-bottom 1.25rem
        .code
          width 7.5rem
</style>
