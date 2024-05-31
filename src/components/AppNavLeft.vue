<script>
export default {
  name: "AppNavLeft",
  data() {
    return {
      menu: [
        {
          name: "Donna",
          link: "#",
        },
        {
          name: "Uomo",
          link: "#",
        },
        {
          name: "Bambini",
          link: "#",
        },
      ],
    };
  },
};
</script>

<template>
  <nav>
    <div class="burger"><i class="fa fa-bars"></i></div>
    <ul>
      <li v-for="item in menu">
        <a :href="item.link">{{ item.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
ul {
  list-style-type: none;
  li {
    display: inline-block;
    font-weight: bold;
    a {
      color: white;
      text-decoration: none;
      padding-right: 10px;
      display: inline-block;
    }
  }
}

@media screen and (max-width: 1920px) {
  .burger {
    display: none;
  }
}

@media screen and (max-width: 540px) {
  ul {
    display: none;
  }
  .burger {
    display: block;
    font-size: 25px;
    color: #ffffff;
    cursor: pointer;
  }
}
</style>
