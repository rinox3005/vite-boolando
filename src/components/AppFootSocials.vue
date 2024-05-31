<script>
export default {
  name: "AppFootSocials",
};
</script>

<template>
  <div class="socials">
    <div class="mb-10 bold white font-size-15">Trovaci anche su</div>
    <div>
      <img
        class="icons-footer pr-5"
        src="/img/twitter-square-icon.webp"
        alt="twitter"
      />
      <img
        class="icons-footer pr-5"
        src="/img/facebook-square-icon-511x512-9dz42ub9.png"
        alt="facebook"
      />
      <img
        class="icons-footer pr-5"
        src="/img/Black_Instagram_icon.svg.png"
        alt="instagram"
      />
      <img
        class="icons-footer pr-5"
        src="/img/pinterest-square-512.webp"
        alt="pinterest"
      />
      <img
        class="icons-footer pr-5"
        src="/img/youtube-square.png"
        alt="youtube"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "/src/assets/styles/partials/variables" as *;
.white {
  color: white;
}
img {
  @extend %white-icons;
  height: 18px;
}

.socials {
  text-align: center;
}
</style>
