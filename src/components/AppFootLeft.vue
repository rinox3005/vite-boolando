<script>
export default {
  name: "AppFootLeft",
};
</script>

<template>
  <div class="white col">
    <div class="mb-10 bold">Boolando s.r.l</div>
    <ul>
      <li>Informazioni legali</li>
      <li>Informativa sulla privacy</li>
      <li>Diritto di recesso</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.white {
  color: white;
}

.bold {
  font-weight: bold;
}

span {
  padding-right: 10px;
  font-size: 12px;
}
ul {
  list-style-type: none;
  display: flex;
  li {
    padding-right: 20px;
  }
}

.foot-menu {
  width: 100%;
}
@media screen and (max-width: 992px) {
  .col {
    width: 100%;
    text-align: center;
    margin-bottom: 20px;
    display: flex;
    flex-direction: column;
  }

  ul {
    text-align: center;
    justify-content: center;
    li {
      padding-left: 15px;
    }
  }
}

@media screen and (max-width: 540px) {
  .col {
    width: 100%;
  }
}
</style>
