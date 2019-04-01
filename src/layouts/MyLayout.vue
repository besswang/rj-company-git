<template>
  <q-layout class="header-con" view="lHh Lpr lFf">
    <q-layout-header class="header">
      <q-toolbar class="bg-transparent text-white">
        <q-toolbar-title>
          <img class="logo" alt="" src="~assets/images/logo.png">
        </q-toolbar-title>
        <q-btn-toggle
        v-model="model"
        flat stretch
        toggle-color="orange"
        :options="[
          {label: '首页', value: 1},
          {label: '服务', value: 2},
          {label: '案例', value: 3},
          {label: '观点', value: 4},
          {label: '关于', value: 5}
        ]"
        />
      </q-toolbar>
    </q-layout-header>
    <q-page-container style="padding-top:0">
      <router-view />
    </q-page-container>
    <div class="shade bg-black"></div>
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
      model: 1,
      leftDrawerOpen: this.$q.platform.is.desktop
    }
  },
  methods: {
    openURL
  }
}
</script>

<style lang="stylus">
.header-con
  .shade
    position:fixed
    width:100%
    height:110px
    left:0
    top:0
    z-index 99
    opacity :.4
  .header
    padding:30px 0
    .logo
      height:2em
</style>
