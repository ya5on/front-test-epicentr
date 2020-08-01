<template>
  <div>
    <carousel :perPage="1"
              :navigationEnabled="true"
              :navigationNextLabel="nextLabel"
              :navigationPrevLabel="prevLabel">
      <slide>
        <img src="../assets/img/download-5.png" alt="">
      </slide>
      <slide>
        <img src="../assets/img/download-3.png" alt="">
      </slide>
      <slide>
        <img src="../assets/img/download-4.png" alt="">
      </slide>
    </carousel>
  </div>
</template>

<script>
export default {
  name: "Carousell",
  data() {
    return {
      nextLabel: ">",
      prevLabel: "<"
    }
  }
}
</script>

<style lang="sass">
.VueCarousel-dot
  width: 18px !important
  height: 3px !important
  background-color: #D7D7D7 !important
  padding: 2px !important
  outline: none !important

  &--active
    background-color: $main-color !important

.VueCarousel-navigation
  position: relative
  margin: 0 auto
  width: 70px
  height: 30px

  &-button
    top: auto !important
    margin-top: 20px
    font-weight: 600
    font-size: 16px

  &-prev
    left: -10px !important
    transform: initial !important


  &-next
    right: -10px !important
    transform: initial !important


</style>