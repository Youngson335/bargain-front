<template>
  <header class="vue-header container">
    <vue-menu class="vue-header__menu" />
    <vue-content-header />
  </header>
</template>
<script lang="ts" setup>
import VueMenu from "../Menu/VueMenu.vue";
import VueContentHeader from "./VueContentHeader.vue";
</script>
<style lang="scss">
.vue-header {
  &__menu {
    margin: 10px 0px;
  }
}
</style>
