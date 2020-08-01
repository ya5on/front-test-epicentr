<template>
  <main class="main">
    <div class="container">
      <header class="header">
        <div class="cart">
          <img class="cart__img" src="../assets/img/cart.png" alt="">
          <span class="cart__price">2</span>
        </div>
      </header>
      <div class="content">
        <div class="content__inner">
          <div class="content__slider">
            <div class="brand">
              <img src="../assets/img/brand.jpg" alt="">
            </div>
            <div class="slider">
              <Carousel/>
              <img class="slider__hand" src="../assets/img/hand.png" alt="">
            </div>
          </div>
          <div class="content__text">
            <div class="code">
              <p class="code__model">Model: 505795</p>
              <img src="../assets/img/spec.png" alt="">
            </div>
            <div class="title">
              <h2>MOMENTUM<span>®</span><br><span>Wireless Black</span></h2>
            </div>
            <div class="subtitle">
              <h3>Wireless headphones with integrated microphone</h3>
            </div>
            <div class="description">
              Peak performance with active noise cancelation. Sennheiser's new MOMENTUM Wireless - Closed circumaural
              headphone featuring <span>Bluetooth®</span> wireless technology and NoiseGard Hybrid active noise
              cancelation
            </div>
            <div class="rate">
              <div class="rating">
                <div class="rating-area">
                  <input type="radio" id="star-5" name="rating" value="5">
                  <label for="star-5" title="Оценка «5»"></label>
                  <input type="radio" id="star-4" name="rating" value="4">
                  <label for="star-4" title="Оценка «4»"></label>
                  <input type="radio" id="star-3" name="rating" value="3">
                  <label for="star-3" title="Оценка «3»"></label>
                  <input type="radio" id="star-2" name="rating" value="2">
                  <label for="star-2" title="Оценка «2»"></label>
                  <input type="radio" id="star-1" name="rating" value="1">
                  <label for="star-1" title="Оценка «1»"></label>
                </div>
              </div>
              <p class="rating__count">4.25</p>
              <p class="rating__reviews">
                (153 reviews)
              </p>
            </div>
            <div class="price">
              <p class="price__value">$499.95</p>
              <p class="price__text">Shipping and taxes extra</p>
            </div>
            <div class="add">
              <div class="quantity">
                <p>Quantity</p>
                <div class="cnt">
                  {{ count }}
                </div>
                <div class="box">
                  <div class="inc" @click="inc">
                    <button>
                      <img src="../assets/img/inc.png" alt="">
                    </button>
                  </div>
                  <div class="dec" @click="dec" v-if="count >= 1">
                    <button>
                      <img class="img-dec" src="../assets/img/inc.png" alt="">
                    </button>
                  </div>
                  <div class="dec" v-else>
                    <button>
                      <img src="../assets/img/dec-noactive.png" alt="">
                    </button>
                  </div>
                </div>
              </div>
              <button class="btn" @click="checkout = true">Add to Cart</button>
            </div>
            <div class="sidebar" v-if="checkout">
              <div class="sidebar__body">
                <button class="sidebar__close" @click="checkout = false">&#x2718;</button>
                <div class="cart">
                  <div style="position: relative; display: inline-block">
                    <img class="cart__img" src="../assets/img/dark-cart.png" alt="">
                    <span class="cart__price">2</span>
                  </div>
                  <div class="cart__total-price">
                    <div class="cart__subtotal">
                      <p>Subtotal (<span>1</span> item):</p>
                      <p class="total">$499.95</p>
                    </div>
                  </div>
                </div>
                <div class="product">
                  <div class="product__item">
                    <button class="product__close">
                      <img src="../assets/img/close.png" alt="">
                    </button>
                    <img class="product__img" src="../assets/img/download-5.png" alt="">
                    <p class="product__title">MOMENTUM® <br> Wireless Black</p>
                    <p class="product__price">$499.95</p>
                    <div class="add">
                      <div class="quantity">
                        <div class="cnt">
                          {{ count }}
                        </div>
                        <div class="box">
                          <div class="inc" @click="inc">
                            <button>
                              <img src="../assets/img/inc.png" alt="">
                            </button>
                          </div>
                          <div class="dec" @click="dec" v-if="count >= 1">
                            <button>
                              <img class="img-dec" src="../assets/img/inc.png" alt="">
                            </button>
                          </div>
                          <div class="dec" v-else>
                            <button>
                              <img src="../assets/img/dec-noactive.png" alt="">
                            </button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="product__item">
                    <button class="product__close">
                      <img src="../assets/img/close.png" alt="">
                    </button>
                    <img class="product__img" src="../assets/img/download-5.png" alt="">
                    <p class="product__title">MOMENTUM® <br> Wireless Black</p>
                    <p class="product__price">$499.95</p>
                    <div class="add">
                      <div class="quantity">
                        <div class="cnt">
                          {{ count }}
                        </div>
                        <div class="box">
                          <div class="inc" @click="inc">
                            <button>
                              <img src="../assets/img/inc.png" alt="">
                            </button>
                          </div>
                          <div class="dec" @click="dec" v-if="count >= 1">
                            <button>
                              <img class="img-dec" src="../assets/img/inc.png" alt="">
                            </button>
                          </div>
                          <div class="dec" v-else>
                            <button>
                              <img src="../assets/img/dec-noactive.png" alt="">
                            </button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="sidebar__footer">
                  <p>Your order qualifies for FREE Shipping <br>
                    Choose this option at checkout. <br>
                    See details</p>
                  <button class="btn">Proceed to checkout</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Carousel from './Carousel'

export default {
  name: 'HelloWorld',
  components: {
    Carousel
  },
  data() {
    return {
      count: 1,
      checkout: false
    }
  },
  methods: {
    inc() {
      this.count += 1
    },
    dec() {
      this.count -= 1
    },
    toggle() {
      this.checkout = !this.checkout
    },
  },
}
</script>

<style lang="sass">
.main
  background: url(../assets/img/0.jpg) no-repeat center
  background-size: cover
  padding-bottom: 211px
  position: relative

.header
  display: flex
  justify-content: flex-end
  +lg(padding-top, 70px)
  +lg(padding-bottom, 50px)

  .cart
    position: relative

    &__img
      padding: 10px 13px 10px 0
      +xs(padding, 15px 13px 15px 0)
      +md(padding, 21px 24px 21px 0)


    &__price
      content: ""
      position: absolute
      top: 3px
      right: 3px
      width: 20px
      height: 20px
      border-radius: 50%
      background-color: $main-color
      z-index: 2
      color: #fff
      font-size: 12px
      display: flex
      justify-content: center
      align-items: center
      +md(top, 10px)
      +md(right, 15px)

.content
  background: url(../assets/img/rec-4.jpg) no-repeat
  background-size: cover
  max-width: 800px
  margin: 0 auto
  min-height: 600px

  &__inner
    display: flex
    flex-direction: column
    +sm(flex-direction, row)


  &__slider
    width: 100%
    +size-sm(6.7)

    .slider
      width: 100%
      position: relative

      &__hand
        position: absolute
        bottom: 0
        right: 50%
        transform: translateX(50%)

      img
        display: block
        margin: 30px auto

  &__text
    padding: 15px 5px
    position: relative
    +size-sm(5.3)
    +sm(display, flex)
    +sm(flex-direction, column)
    +sm(justify-content, space-between)
    +sm(margin-top, 48px)


    .code
      display: flex
      justify-content: space-between
      align-items: center
      margin-bottom: 10px

      &__model
        font-size: 12px
        color: #263238

    .title
      text-align: left
      margin-bottom: 10px
      color: #263238

      h2
        font-weight: 500
        font-size: 21px

      span
        font-size: 16px

    .subtitle
      color: #646B6F
      margin-bottom: 10px
      font-size: 17px
      line-height: 24px

    .description
      color: #263238
      margin-bottom: 10px
      font-size: 14px
      font-weight: 500
      line-height: 23px

      span
        color: $main-color

    .rate
      display: flex
      align-items: center
      margin-bottom: 10px

      .rating
        margin-right: 10px
        +sm(margin-right, 40px)

        &__count
          color: #F14560
          font-size: 15px
          +sm(margin-right, 6px)

        &__reviews
          font-size: 12px
          margin-right: 5px

      .rating-area
        overflow: hidden

      .rating-area:not(:checked) > input
        display: none

      .rating-area:not(:checked) > label
        float: right
        width: 12px
        height: 12px
        border-radius: 50%
        background-color: #CCCCCC
        padding: 0
        cursor: pointer
        color: #CCCCCC
        text-shadow: 1px 1px #bbb
        margin-right: 5px

      .rating-area:not(:checked) > label:before
        content: ''

      .rating-area > input:checked ~ label
        background-color: #FCCF47

      .rating-area:not(:checked) > label:hover,
      .rating-area:not(:checked) > label:hover ~ label
        background-color: #FCCF47

      .rating-area > input:checked + label:hover,
      .rating-area > input:checked + label:hover ~ label,
      .rating-area > input:checked ~ label:hover,
      .rating-area > input:checked ~ label:hover ~ label,
      .rating-area > label:hover ~ input:checked ~ label
        background-color: #FCCF47

      .rate-area > label:active
        position: relative

    .price
      margin-bottom: 10px

      &__value
        font-size: 26px
        color: #F14560

      &__text
        font-size: 12px
        color: #646B6F


.add
  display: flex
  justify-content: space-between
  padding-bottom: 60px
  +sm(padding-bottom, 0)

  .quantity
    display: flex
    align-items: center

    p
      font-size: 14px
      color: #263238
      margin-right: 8px

    .cnt
      border: 1px solid #DDDDDD
      width: 52px
      height: 46px
      display: flex
      justify-content: center
      align-items: center
      font-size: 18px

    .box
      display: flex
      flex-direction: column
      justify-content: space-between
      height: 44px

      .inc, .dec
        padding: 0 5px

        button
          background: initial
          border: none
          outline: none
          cursor: pointer

        .img-dec
          transform: rotate(180deg)

  .btn
    width: 100%
    max-width: 150px
    background-color: $main-color
    border: none
    outline: none
    color: #fff
    font-size: 17px
    cursor: pointer


.sidebar
  width: 100%
  height: 100%
  background-color: rgba(0, 0, 0, .5)
  position: fixed
  top: 0
  right: 0
  z-index: 3
  transition: all .3s ease
  display: flex
  justify-content: center
  align-items: center

  &__body
    width: 300px
    height: 540px
    background-color: #fff
    position: relative
    display: flex
    flex-direction: column
    align-items: center
    justify-content: space-between
    +sm(width, 370px)
    +sm(height, 620px)
    +lg(height, 100%)
    +lg(position, absolute)
    +lg(right, 0)

    .cart
      margin-top: 10px
      display: flex
      justify-content: center
      align-items: center
      +md(margin-top, 50px)
      +lg(margin-top, 70px)

      &__img
        padding: 10px 13px 10px 0

      &__price
        content: ""
        position: absolute
        top: 3px
        right: 3px
        width: 20px
        height: 20px
        border-radius: 50%
        background-color: $main-color
        z-index: 2
        color: #fff
        font-size: 12px
        display: flex
        justify-content: center
        align-items: center

      &__total-price
        display: flex
        flex-direction: column
        margin-left: 30px

      &__subtotal
        font-size: 12px
        color: #37474f

        .total
          font-size: 18px
          color: #263238

  .product
    width: 100%
    max-width: 230px
    margin: 0 auto
    display: flex
    flex-direction: column

    &__item
      position: relative
      display: flex
      flex-direction: column
      align-items: center
      margin-top: 10px
      +sm(margin-top, 30px)

    &__close
      position: absolute
      top: 0
      right: 0
      cursor: pointer
      background: initial
      border: none

    &__img
      max-width: 70px
      margin-bottom: 10px
      +lg(margin-bottom, 25px)


    &__title
      font-size: 16px
      color: #646b6f
      margin-bottom: 5px
      +lg(margin-bottom, 20px)

    &__price
      color: #263238
      font-size: 12px
      font-weight: 500
      margin-bottom: 5px
      +lg(margin-bottom, 20px)

    .add
      padding-bottom: 10px
      display: none
      +lg(display, initial)

  &__close
    background: initial
    border: none
    font-size: 20px
    padding: 5px
    position: absolute
    top: 5px
    left: 15px
    cursor: pointer



  &__footer
    width: 100%
    max-width: 230px
    margin: 0 auto
    text-align: center
    font-size: 12px

    .btn
      width: 100%
      max-width: 230px
      background-color: $main-color
      border: none
      outline: none
      color: #fff
      font-size: 17px
      cursor: pointer
      padding: 15px 34px
      margin-bottom: 15px
      +lg(margin-bottom, 60px)
      +lg(margin-top, 25px)

    p
      display: none
      color: #b3b6b8
      +lg(display, initial)



</style>
