<script>
import AppMain from "./components/AppMain.vue";
import AppHeader from "./components/AppHeader.vue";
export default {
  name: "App",
  data() {
    return {};
  },
  components: {
    AppHeader,
    AppMain,
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <footer></footer>
</template>

<style lang="scss" scoped></style>
