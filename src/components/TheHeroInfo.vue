<template>
  <div class="hero-info"
       :style="{backgroundColor: background}">
    <div class="hero-info-text">
      <h2 class="hero-info__title"
          :style="{color: colorTitle}">
        {{ title }}
      </h2>
      <span
          :style="{color: colorDescription}"
          class="hero-info__description">
          {{ description }}
        </span>
    </div>
    <the-button
        color="secondary"
        type="link" to="/"
    >
      View collection
    </the-button>
<!--    <a :href="link"-->
<!--       class="hero-info-link"-->
<!--       :style="{color: colorLink}"-->
<!--    >View collection</a>-->
  </div>
</template>

<script setup>
import TheButton from '../components/ui/TheButton.vue'
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
    align-items: flex-start;
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
  }
}
</style>