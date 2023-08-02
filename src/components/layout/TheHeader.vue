<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-search">
        <img src="/svg/search.svg" alt="search">
      </div>
      <router-link to="/" class="header-logo">Avion</router-link>
      <div class ="header-top-right">
        <div class="header-top-right_cart">
          <router-link to="/cart">
            <img src="/svg/cart.svg" alt="">
          </router-link>
        </div>
        <div class="header-top-right_user">
          <router-link to="/user">
            <img src="/svg/user.svg" alt="">
          </router-link>
        </div>
      </div>
    </div>
    <div class="header-menu">
      <router-link :href="element.path"
         v-for="(element, i) of menu"
         :key="i"
         class="header-menu__link"
      >{{element.name}}</router-link>
    </div>
  </header>
</template>

<script setup>
import {ref} from "vue";

const menu = [
  {
    name: 'Plant pots',
    path: '/plant'
  },
  {
    name: 'Ceramics',
    path: '/ceramics'
  },
  {
    name: 'Tables',
    path: '/tables'
  },
  {
    name: 'Chairs',
    path: '/chairs'
  },
  {
    name: 'Crockery',
    path: '/crockery'
  },
  {
    name: 'Tableware',
    path: '/tableware'
  },
  {
    name: 'Cutlery',
    path: '/cutlery'
  }
]
</script>

<style lang="scss" scoped>
    .header {
      height: 132px;
      background: #fff;
      &-top {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        height: 70px;
        align-items: center;
        border-bottom: 1px solid #D9D9D9;
        margin: 0 28px;
        &-right {
          display: flex;
          align-items: center;
          justify-content: flex-end;
          &_cart {
            margin-right: 16px;
          }
        }
      }
      &-logo {
        color: var(--black);
        font-family: var(--metro);
        text-decoration: none;
        text-align: center;
        &:hover{
          text-decoration: underline;
        }
      }
      &-menu {
        height: 62px;
        display: flex;
        justify-content: center;
        align-items: center;
        &__link {
          margin: 0 22px;
          color: var(--gray);
          text-decoration: none;
          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
</style>