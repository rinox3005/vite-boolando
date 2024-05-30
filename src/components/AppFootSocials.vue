<script>
export default {
  name: "AppFootSocials",
};
</script>

<template>
  <div>
    <div class="mb-10 bold white pr-20 font-size-12">Trovaci anche su</div>
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
.white {
  color: white;
}
img {
  height: 14px;
  filter: brightness(0) saturate(100%) invert(100%) sepia(0%) saturate(0%)
    hue-rotate(275deg) brightness(105%) contrast(106%);
}
</style>
