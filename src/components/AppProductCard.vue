<script>
export default {
  name: "AppProductCard",
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
};
</script>

<template>
  <div class="content">
    <img class="main-img" :src="product.image" :alt="product.name" />
    <img class="hover-img" :src="product.alternativeImg" :alt="product.name" />
    <div class="heart">&hearts;</div>
    <div class="label">
      <span class="discount bold" v-show="product.discount">{{
        product.discount
      }}</span>
      <span class="sustainability bold" v-show="product.eco">{{
        product.eco
      }}</span>
    </div>
  </div>
  <div class="brand">{{ product.brand }}</div>
  <div class="product uppercase bold">{{ product.name }}</div>
  <div class="price">
    <span class="red-text bold">{{ product.price }}</span>
    <span class="line-through">{{ product.previousPrice }}</span>
  </div>
</template>

<style lang="scss" scoped>
@import "/src/assets/styles/partials/variables";

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

.heart:hover {
  color: $heart-color;
  cursor: pointer;
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
</style>
