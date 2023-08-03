<template>
  <button
      v-if="type === 'button'"
      :class="['btn',
      {'btn--primary' :color === 'primary',
        'btn--secondary' :color === 'secondary',
          'btn--lightgray' :color === 'lightgray'}]">
    <slot/>
  </button>
  <router-link
      v-else
      :class="['btn',
      {'btn--primary' :color === 'primary',
        'btn--secondary' :color === 'secondary',
          'btn--lightgray' :color === 'lightgray'}]"
      :to="to"
      :style="{backgroundColor: background}">
    <slot/>
  </router-link>
</template>

<script setup>
const props = defineProps({
  background:{
    type: String,
    required: false
  },
  type:{
    type: String,
    default: 'button'
  },
  to:{
    type: String,
    required: false
  },
  color:{
    type: String,
    default: 'primary'
  }
})
</script>

<style lang="scss" scoped>
.btn{
    padding: 0 32px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    border: none;
    font-size: 16px;
    height: 56px;
    width: 170px;
    text-decoration: none;
    &:hover {
      opacity: 0.8;
    }
    &--primary {
      background: var(--black);
      color: #fff;
    }
    &--secondary {
      background: #4E4D93;
      color: #fff;
    }
    &--lightgray {
      background: #F9F9F9;
      color: #2A254B;
    }
  }

</style>