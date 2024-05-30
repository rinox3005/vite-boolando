<script>
import AppNavLeft from "./components/AppNavLeft.vue";
import AppNavRight from "./components/AppNavRight.vue";
import AppNavLogo from "./components/AppNavLogo.vue";
export default {
  name: "App",
  data() {
    return {};
  },
  components: {
    AppNavLeft,
    AppNavRight,
    AppNavLogo,
  },
};
</script>

<template>
  <header>
    <div class="row container">
      <div class="row col-33 align-center"><AppNavLeft /></div>
      <div class="row col-33 justify-center"><AppNavLogo /></div>
      <div class="row col-33 justify-end align-center"><AppNavRight /></div>
    </div>
  </header>
  <main></main>
  <footer></footer>
</template>

<style lang="scss" scoped></style>
