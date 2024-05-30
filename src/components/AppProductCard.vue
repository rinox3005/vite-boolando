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

<style lang="scss" scoped></style>
