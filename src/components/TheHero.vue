<template>
  <div class="hero">
    <div class="hero-info">
      <the-hero-info
        title="Luxury homeware for people who love timeless design quality"
        description="Shop the new Spring 2023 collection today"
        link="#"/>
    </div>
  </div>
</template>

<script setup>
import TheHeroInfo from './TheHeroInfo.vue'
</script>

<style lang="scss" scoped>
.hero {
  background: url("/img/hero.jpg");
  height: 704px;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 80px;
  &-img{
    max-width: 100%;
  }
}
</style>