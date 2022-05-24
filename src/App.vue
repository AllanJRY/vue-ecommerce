<template>
  <div id="app">
    <TheHeader />
    <CartProductList />
  </div>
</template>

<script>
import CartProductList from './components/CartProductList.vue';
import TheHeader from "./components/TheHeader.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    CartProductList,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
