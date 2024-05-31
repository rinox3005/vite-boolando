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
        <div class="col" v-for="product in products.products">
          <AppProductCard :product="product" />
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;

main {
  padding-top: 90px;
  padding-bottom: 40px;
}

.container {
  @extend %container;
}

.row {
  @extend %flex;
}

.col {
  @extend %col;
  margin: 20px;
}

@media screen and (max-width: 992px) {
  .col {
    width: calc((100% / 2) - 40px);
  }
}

@media screen and (max-width: 540px) {
  .col {
    width: 100%;
  }
}
</style>
