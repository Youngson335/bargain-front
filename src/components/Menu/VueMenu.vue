<template>
  <nav class="vue-menu block-radius">
    <div class="vue-menu__items">
      <div class="vue-menu-logo">
        <vue-menu-link> logo </vue-menu-link>
      </div>
      <div class="vue-menu-links">
        <div v-for="item of menuItems">
          <vue-menu-link> {{ item.title }} </vue-menu-link>
        </div>
        <vue-phone-link> + 7 999 999 99 99 </vue-phone-link>
      </div>
    </div>
  </nav>
</template>
<script lang="ts" setup>
import VueMenuLink from "../Link/VueMenuLink.vue";
import VuePhoneLink from "../Link/VuePhoneLink.vue";

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
  background-color: $gray;
  padding: 10px;
  &-logo {
    display: flex;
    align-items: center;
  }
  &-links {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
  }
  &__items {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
