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
  <footer class="foot">
    <div class="row container justify-between">
      <AppFootLeft />
      <AppFootSocials />
    </div>
  </footer>
</template>

<style lang="scss" scoped></style>
