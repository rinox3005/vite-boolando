<script>
import AppNavLeft from "./AppNavLeft.vue";
import AppNavRight from "./AppNavRight.vue";
import AppNavLogo from "./AppNavLogo.vue";
export default {
  name: "AppHeader",
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
</template>

<style lang="scss" scoped></style>
