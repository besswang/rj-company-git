<template>
  <q-layout class="header-con" view="lHh Lpr lFf">
    <Header />
    <q-page-container style="padding-top:0">
      <router-view />
    </q-page-container>
    <Footer />
    <!-- <q-layout-footer>
      底部
    </q-layout-footer> -->
  </q-layout>
</template>

<script>
import { openURL } from 'quasar'
import Header from './Header.vue'
import Footer from './Footer.vue'
export default {
  name: 'MyLayout',
  components: {
    Header,
    Footer
  },
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
