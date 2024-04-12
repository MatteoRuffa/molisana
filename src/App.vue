<template>
  <HeaderComponents />
  <MainComponents />
  <FooterComponents />
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponents from './components/MainComponents.vue';
import FooterComponents from './components/FooterComponents.vue';
  export default {
    name: 'App',
    components: {
      HeaderComponents,
      MainComponents,
      FooterComponents,
      
    }
  }
</script>

<style lang="scss" scoped>
h1{
  color: red;
}
</style>