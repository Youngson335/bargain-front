<template>
  <nav class="vue-menu">
    <div>
      <div>
        <vue-menu-link> logo </vue-menu-link>
      </div>
      <div v-for="item of menuItems"></div>
    </div>
  </nav>
</template>
<script lang="ts" setup>
import VueMenuLink from "../Link/VueMenuLink.vue";

const menuItems = [
  {
    id: 1,
    route: "/",
    title: "ссылка",
  },
  {
    id: 2,
    route: "/",
    title: "ссылка",
  },
  {
    id: 3,
    route: "/",
    title: "ссылка",
  },
];
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-menu {
  background-color: $menu;
}
</style>
