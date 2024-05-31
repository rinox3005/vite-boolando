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
  padding: 40px 0;
}
.container {
  @extend %container, %flex;
  justify-content: space-between;
  padding: 0 20px;
}

@media screen and (max-width: 992px) {
  .container {
    justify-content: center;
  }
}

@media screen and (max-width: 540px) {
  .col {
    width: 100%;
  }
}
</style>
