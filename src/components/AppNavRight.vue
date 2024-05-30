<script>
export default {
  name: "AppNavRight",
};
</script>

<template>
  <a href="#"><img src="/img/user.webp" alt="user" /></a>
  <a href="#"><img src="/img/heart.webp" alt="favourites" /></a>
  <a href="#"><img src="/img/shopping-bag.webp" alt="shop" /></a>
</template>

<style lang="scss" scoped>
a {
  img {
    height: 18px;
    padding-left: 8px;
    filter: brightness(0) saturate(100%) invert(100%) sepia(0%) saturate(0%)
      hue-rotate(275deg) brightness(105%) contrast(106%);
  }
}
</style>
