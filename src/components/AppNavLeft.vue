<script>
export default {
  name: "AppNavLeft",
};
</script>

<template>
  <ul>
    <li>
      <a href="#">Donna</a>
    </li>
    <li>
      <a href="#">Uomo</a>
    </li>
    <li>
      <a href="#">Bambini</a>
    </li>
  </ul>
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
    }
  }
}
</style>
