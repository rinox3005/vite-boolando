<script>
import AppFootLeft from "./AppFootLeft.vue";
import AppFootSocials from "./AppFootSocials.vue";
export default {
  name: "AppFooter",
  components: {
    AppFootLeft,
    AppFootSocials,
  },
};
</script>

<template>
  <footer>
    <div class="container">
      <AppFootLeft />
      <AppFootSocials />
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;

footer {
  width: 100%;
  background-color: $bg-footer;
  padding: 30px 100px;
}
.container {
  @extend %container, %flex;
  justify-content: space-between;
}
</style>
