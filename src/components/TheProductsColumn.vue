<template>
  <div class="products-container">
    <div class="products">
      <the-products
          v-for="product of products"
          :key="product.id"
          :img="product.img"
          :name="product.name"
          :price="product.price"/>
    </div>
    <a class="products-link" href="">View collection</a>
  </div>
</template>

<script setup>
import {ref} from "vue";
import TheProducts from  '../components/TheProduct.vue'


const products = ref([
  {
    id: 1,
    img:'/img/product-1.jpg',
    name:'The Dandy chair',
    price: 250
  },
  {
    id: 2,
    img:'/img/product-2.jpg',
    name:'Rustic Vase Set',
    price: 155
  },
  {
    id: 3,
    img:'/img/product-3.jpg',
    name:'The Silky Vase',
    price: 125
  },
  {
    id: 4,
    img:'/img/product-4.jpg',
    name:'The Lucy Lamp',
    price: 399
  }
])
</script>

<style lang="scss" scoped>
.products {
  display: flex;
  grid-template-columns: repeat(4, 1fr);
  column-gap: 20px;
  padding: 0 80px;
  margin-bottom: 56px;
  &-container {
    margin-bottom: 64px;
  }
  &-link {
    display: block;
    text-align: center;
    color: var(--black);
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
}
</style>