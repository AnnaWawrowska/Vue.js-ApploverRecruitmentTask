<template lang="html">
  <section class="section--offers">
    <div class="container">
      <ul class="allOffers">
        <li v-for="n in 6">
          <offer></offer>
        </li>
      </ul>
      <ul class="slider__nav">
        <li><button class="slider__arrow slider__arrow--prev"></button> </li>
        <li><button class="slider__arrow slider__arrow--next"></button> </li>
      </ul>
    </div>
  </section>
</template>

<script>
import Offer from './Offer.vue'
export default {
  components: {
    'offer': Offer
  },
  mounted() {
    $('.allOffers').slick({
      centerMode: true,
      slidesToShow: 3,
      variableWidth: true,
      prevArrow: '.slider__arrow--prev',
      nextArrow: '.slider__arrow--next',
      swipe: false,
      responsive: [
        {
          breakpoint: 768,
          settings: {
            centerMode: true,
            centerPadding: '0',
            slidesToShow: 1,
            variableWidth: false,
            swipe: true,
          }
        },
      ]
    });
  }
}
</script>

<style lang="scss" scoped>
@import '../styles/helpers/colors.scss';
@import '../styles/helpers/include-media.scss';

.slider {
  &__nav {
    @include media('<lg') {
      display: flex;
      justify-content: space-around;
      width: 80%;
      margin: 0 auto;
    }
  }
  &__arrow {
    width: 69px;
    height: 69px;
    background-color: transparent;
    background-size: contain;
    position: absolute;
    top: 43%;
    outline: 0;
    cursor: pointer;
    border-radius: 50%;
    box-shadow: 0;
    transition: box-shadow 0.3s ease;
    @include media('<lg') {
      width: 50px;
      height: 50px;
      top: 0;
      position: relative;
      margin: 50px 0 30px;
    }
    @include media('<sm') {
      margin-top: 20px;
    }

    &:focus {
      outline: 0;
    }

    &:hover {
      box-shadow: 0 2px 30px 0 rgba(0,0,0,0.6);
    }

    &--prev {
      background-image: url(../assets/svg/ico-arrow-left.svg);
      left: 7%;
      @include media('<xl') {
        left: 2%;
      }
      @include media('<lg') {
        left: 0;
      }
    }

    &--next {
      background-image: url(../assets/svg/ico-arrow-right.svg);
      right: 7%;
      @include media('<xl') {
        right: 2%;
      }
      @include media('<lg') {
        right: 0;
      }
    }
  }
}
</style>
