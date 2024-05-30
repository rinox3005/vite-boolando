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
    <div class="container">
      <div><AppNavLeft /></div>
      <div class="justify-center"><AppNavLogo /></div>
      <div class="justify-end"><AppNavRight /></div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import "/src/assets/styles/partials/variables";

header {
  position: fixed;
  background-color: $bg-header;
  box-shadow: 0 2px rgba(158, 157, 157, 0.63);
  width: 100%;
  z-index: 1;
}
.container {
  display: flex;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 0 auto;

  div {
    display: flex;
    flex-wrap: wrap;
    width: calc(33.3333333333% - 40px);
    margin: 20px;
    align-content: center;
  }
}
</style>
