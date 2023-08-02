<template>
  <div class="container">
    <the-header/>
    <the-hero/>
    <the-about/>
    <the-products-column/>
    <the-ideas/>
  </div>
</template>

<script setup>
import TheHeader from "../components/layout/TheHeader.vue";
import TheHero from "../components/TheHero.vue";
import TheAbout from "../components/TheAbout.vue";
import TheProductsColumn from "../components/TheProductsColumn.vue";
import TheIdeas from "../components/TheIdeas.vue";
</script>