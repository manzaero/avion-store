<template>
  <div class="ideas">
    <the-hero-info
      title="It started with a small idea"
      description="A global brand with local beginnings, our story begain in a small studio in South London in early 2014"
      background="var(--black)"
      color-title="#fff"
      color-description="#fff"
      color-link="#fff"
    />
    <img src="/img/room.jpg" alt="">
  </div>
</template>

<script setup>
import TheHeroInfo from './TheHeroInfo.vue'
</script>

<style lang="scss" scoped>
.ideas {
  padding: 0 80px;
  margin-bottom: 60px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  column-gap: 16px;
}
</style>