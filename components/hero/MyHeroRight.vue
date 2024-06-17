<template>
  <div class="hero-right">
    <img class="hero-right_img" :src="heroImg" alt="hero-img" />
  </div>
</template>

<script setup>
const heroImg = "/svg/hero.svg";
</script>

<style lang="scss" scoped>
.hero-right {
  margin-top: 34px;
}

@media (max-width: 550px) {
  .hero-right_img {
    width: 100%;
  }
}
</style>
