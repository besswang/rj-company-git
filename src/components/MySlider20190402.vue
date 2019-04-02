<template>
  <div class="carousel-con">
    <q-carousel
      class="q-panel-parent"
      animated
      v-model="slide"
      navigation
      infinite
      autoplay
    >
      <q-carousel-slide :name="1" img-src="https://cdn.quasar-framework.org/img/mountains.jpg" />
      <q-carousel-slide :name="2" img-src="https://cdn.quasar-framework.org/img/parallax1.jpg" />
      <q-carousel-slide :name="3" img-src="https://cdn.quasar-framework.org/img/parallax2.jpg" />
      <q-carousel-slide :name="4" img-src="https://cdn.quasar-framework.org/img/quasar.jpg" />
    </q-carousel>
  </div>
</template>

<script>
export default {
  name: 'MySlider',
  data () {
    return {
      slide: 1
    }
  },
  methods: {

  }
}
</script>

<style lang="stylus">
.carousel-con
  height 80vh
  width 100%
  .q-panel-parent
    width 100%
    height 100%
</style>
