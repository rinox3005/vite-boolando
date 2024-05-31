<script>
import AppProductCard from "./AppProductCard.vue";
export default {
  name: "AppMain",
  data() {
    return {
      products: [
        {
          name: "relaxed fit tee unisex",
          brand: "Levi's",
          image: "/img/1.webp",
          alternativeImg: "/img/1b.webp",
          price: "14.99 €",
          previousPrice: "29.99 €",
          discount: "-50%",
          eco: "Sostenibilitá",
        },
        {
          name: "roses tee",
          brand: "Guess",
          image: "/img/2.webp",
          alternativeImg: "/img/2b.webp",
          price: "20.99 €",
          previousPrice: "29.99 €",
          discount: "-30%",
          eco: "",
        },
        {
          name: "voglia di colori pastello",
          brand: "Come Zucchero Filato",
          image: "/img/3.webp",
          alternativeImg: "/img/3b.webp",
          price: "129.99 €",
          previousPrice: "184.99 €",
          discount: "-30%",
          eco: "",
        },
        {
          name: "tee unisex",
          brand: "Levi's",
          image: "/img/4.webp",
          alternativeImg: "/img/4b.webp",
          price: "14.99 €",
          previousPrice: "29.99 €",
          discount: "-50%",
          eco: "Sostenibilitá",
        },
        {
          name: "stripe bodice",
          brand: "Maya Deluxe",
          image: "/img/5.webp",
          alternativeImg: "/img/5b.webp",
          price: "99.99 €",
          previousPrice: "",
          discount: "",
          eco: "",
        },
        {
          name: "maglione - black",
          brand: "Esprit",
          image: "/img/6.webp",
          alternativeImg: "/img/6b.webp",
          price: "29.99 €",
          previousPrice: "",
          discount: "",
          eco: "Sostenibilitá",
        },
      ],
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
        <div class="col-33" v-for="product in products">
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
