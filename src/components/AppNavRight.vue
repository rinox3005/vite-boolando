<script>
export default {
  name: "AppNavRight",
  data() {
    return {
      userMenu: [
        {
          name: "user",
          link: "#",
          img: "/img/user.webp",
        },
        {
          name: "favourites",
          link: "#",
          img: "/img/heart.webp",
        },
        {
          name: "shop",
          link: "#",
          img: "/img/shopping-bag.webp",
        },
      ],
    };
  },
};
</script>

<template>
  <div v-for="item in userMenu">
    <a :href="item.link"><img :src="item.img" :alt="item.name" /></a>
  </div>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;

a {
  img {
    @extend %white-icons;
    height: 18px;
    padding-left: 8px;
  }
}
</style>
