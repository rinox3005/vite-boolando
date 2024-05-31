<script>
export default {
  name: "AppProductCard",
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  methods: {
    switchFavourites() {
      if (this.product.isInFavorites) {
        return (this.product.isInFavorites = false);
      } else {
        return (this.product.isInFavorites = true);
      }
    },
  },
};
</script>

<template>
  <div class="content">
    <img
      class="main-img"
      :src="`/img/${product.frontImage}`"
      :alt="product.name"
    />
    <img
      class="hover-img"
      :src="`/img/${product.backImage}`"
      :alt="product.name"
    />
    <div
      class="heart"
      :class="[
        { fav: product.isInFavorites },
        { notFav: !product.isInFavorites },
      ]"
      @click="switchFavourites()"
    >
      &hearts;
    </div>
    <div class="label">
      <span
        class="discount bold"
        v-for="badge in product.badges"
        v-show="badge.type === 'discount'"
        >{{ badge.value }}</span
      >
      <span
        class="sustainability bold"
        v-for="badge in product.badges"
        v-show="badge.type === 'tag'"
        >{{ badge.value }}</span
      >
    </div>
  </div>
  <div class="brand">{{ product.brand }}</div>
  <div class="product uppercase bold">{{ product.name }}</div>
  <div class="price">
    <span class="red-text bold">{{ product.price }}</span>
    <span class="line-through">{{ product.discount }}</span>
  </div>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;

.brand {
  font-size: 13px;
}

.price {
  font-size: 14px;
}

.red-text {
  color: $price-color;
  margin-right: 4px;
}

.hover-img {
  display: none;
}

.content:hover .hover-img {
  display: inline-block;
}

.content:hover .main-img {
  display: none;
}

.discount {
  background-color: $bg-discount-color;
  padding: 5px 8px;
  color: white;
  font-size: 11px;
  margin-right: 5px;
}

.sustainability {
  background-color: $bg-eco-color;
  padding: 5px 8px;
  color: white;
  font-size: 11px;
}

.product {
  font-size: 13px;
}

.content {
  position: relative;
}

.content img {
  width: 100%;
}

.label {
  position: absolute;
  bottom: 40px;
  left: 0px;
}

.heart {
  position: absolute;
  top: 10px;
  right: 0px;
  text-align: center;
  padding: 1px 11px;
  background-color: white;
  font-size: 30px;
}

.fav {
  color: red;
  cursor: pointer;
  &:hover {
    color: black;
  }
}

.notFav {
  color: black;
  cursor: pointer;
  &:hover {
    color: red;
  }
}
</style>
