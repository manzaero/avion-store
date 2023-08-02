<template>
  <div class="product">
    <a href="" class="product-image">
      <img :src="img" :alt="name">
    </a>
    <a href="" class="product-name">
      {{ name }}
    </a>
    <span class="product-price">£{{ price }}</span>
  </div>
</template>

<script setup>
const props = defineProps({
  img:{
    type: String,
    required: true
  },
  name:{
    type: String,
    required: true
  },
  price:{
    type: Number,
    required: true
  }
})
</script>

<style lang="scss" scoped>
.product {
  &-image {
    display: block;
    margin-bottom: 24px;
  }
  &-name{
    display: block;
    color: var(--black);
    font-size: 14px;
    line-height: 28px;
    font-family: var(--metro);
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
  &-price {
    font-size: 18px;
    color: var(--black);
  }
}
</style>