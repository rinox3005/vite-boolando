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
</style>
