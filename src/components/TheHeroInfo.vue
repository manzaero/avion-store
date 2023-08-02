<template>
  <div class="hero-info"
       :style="{backgroundColor: background}">
    <div
        class="hero-info-text"

    >
      <h2
          class="hero-info__title"
          :style="{color: colorTitle}"
      >
        {{ title }}
      </h2>
      <span
          :style="{color: colorDescription}"
          class="hero-info__description">
          {{ description }}
        </span>
    </div>
    <a :href="link"
       class="hero-info-link"
       :style="{color: colorLink}"
    >View collection</a>
  </div>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: false
  },
  description:{
    type: String,
    required: false
  },
  link:{
    type: String,
    required: false
  },
  colorTitle:{
    type: String,
    default: ''
  },
  colorDescription:{
    type: String,
    default: 'var(--lightGray)'
  },
  background:{
    type: String,
    default: '#fff'
  },
  colorLink: {
    type: String,
    default: ''
  }
})
</script>


<style lang="scss" scoped>
.hero {
  &-info {
    background: #fff;
    max-width: 630px;
    padding: 50px 55px;
    min-height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    &__title{
      font-family: var(--metro);
      font-weight: 400;
      line-height: 1.5;
      margin: 0 0 20px 0;
    }
    &__description {
      color: var(--lightGray);
      font-size: 18px;
    }
    &-link{
      color: var(--black);
      width: 170px;
      height: 56px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      background: rgba(249, 249, 249, 0.15);
      text-decoration: none;
      &:hover {
        background: rgba(249, 249, 249, 0.45);
      }
    }
  }
}
</style>