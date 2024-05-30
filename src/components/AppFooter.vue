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
footer {
  width: 100%;
  background-color: #1a1a1a;
  padding: 30px 100px;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
</style>
