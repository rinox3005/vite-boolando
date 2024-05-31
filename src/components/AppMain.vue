<script>
import products from "/src/assets/data/db.json";
import AppProductCard from "./AppProductCard.vue";
export default {
  name: "AppMain",
  data() {
    return {
      products,
    };
  },
  components: {
    AppProductCard,
  },
};
</script>

<template>
  <main>
    <div class="container">
      <div class="row">
        <div class="col-33" v-for="product in products.products">
          <AppProductCard :product="product" />
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;

main {
  padding-top: 100px;
  padding-bottom: 40px;
}

.container {
  @extend %container;
}

.row {
  @extend %flex;
}

.col-33 {
  @extend %col;
  margin: 20px;
}
</style>
