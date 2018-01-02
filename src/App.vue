<template>
  <div>
    <app-header></app-header>
    <search></search>
    <slider></slider>
    <app-footer></app-footer>
    <modals></modals>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Search from './components/Search.vue';
import Slider from './components/Slider.vue';
import Footer from './components/Footer.vue';
import Modals from './components/Modals.vue';

export default {
  data () {
    return {
    }
  },
  components: {
    'app-header': Header,
    'search': Search,
    'slider': Slider,
    'app-footer': Footer,
    'modals': Modals
  },
}
</script>

<style lang="scss">
  @import './styles/style.scss';
</style>
