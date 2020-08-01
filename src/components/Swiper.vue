<template>
  <div v-swiper:mySwiper="swiperOptions">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <img src="../assets/img/download-5.png" alt="">
      </div>
      <div class="swiper-slide">
        <img src="../assets/img/download-3.png" alt="">
      </div>
      <div class="swiper-slide">
        <img src="../assets/img/download-4.png" alt="">
      </div>
    </div>

  </div>
</template>

<script>
import { directive } from 'vue-awesome-swiper'
export default {
  name: "SwiperSlider",
  data() {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        },
        // Some Swiper option/callback...
      }
    }
  },
  directives: {
    swiper: directive
  },
  computed: {

  },
  mounted() {

  }
}
</script>

<style scoped>


</style>