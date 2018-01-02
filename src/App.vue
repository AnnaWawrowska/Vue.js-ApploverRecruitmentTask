<template>
  <div>
    <app-header></app-header>
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  data () {
    return {
    }
  },
  components: {
    'app-header': Header
  }
}
</script>

<style lang="scss">
  @import './styles/style.scss';
</style>
