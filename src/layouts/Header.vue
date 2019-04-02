<template>
  <div>
    <q-layout-header :class="{head:$q.platform.is.desktop}">
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
        v-if="$q.platform.is.desktop"
        />
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
          v-if="$q.platform.is.mobile"
        >
          <q-icon name="menu" />
        </q-btn>
      </q-toolbar>
    </q-layout-header>

    <q-layout-drawer v-if="$q.platform.is.mobile" v-model="leftDrawerOpen" side="right" :width="200">
      <q-list
        no-border
        link
        inset-delimiter
      >
        <q-item @click.native="openURL('https://discord.gg/5TDhbDg')">
          <q-item-main label="首页"/>
        </q-item>
        <q-item @click.native="openURL('https://discord.gg/5TDhbDg')">
          <q-item-main label="服务"/>
        </q-item>
        <q-item @click.native="openURL('https://discord.gg/5TDhbDg')">
          <q-item-main label="案例"/>
        </q-item>
        <q-item @click.native="openURL('https://discord.gg/5TDhbDg')">
          <q-item-main label="观点"/>
        </q-item>
        <q-item @click.native="openURL('https://discord.gg/5TDhbDg')">
          <q-item-main label="关于"/>
        </q-item>
      </q-list>
    </q-layout-drawer>
    <div class="shade bg-black" :class="{mobile:$q.platform.is.mobile}"></div>
  </div>
</template>

<script>
import { openURL } from 'quasar'
export default {
  name: 'MyLayout',
  data () {
    return {
      model: 1,
      leftDrawerOpen: this.$q.platform.is.desktop,
      isMobile: this.$q.platform.is.mobile
    }
  },
  methods: {
    openURL
  }
}
</script>

<style lang="stylus">
.shade
  position:fixed
  width:100%
  height:110px
  left:0
  top:0
  z-index 125
  opacity .4
.head
  padding 30px 0
.logo
  height 2em
.shade.mobile
  height 3.125rem
</style>
