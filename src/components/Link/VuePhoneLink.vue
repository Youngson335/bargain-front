<template>
  <div class="vue-phone-link">
    <slot />
  </div>
</template>
<script lang="ts" setup></script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-phone-link {
  padding: 10px 20px;
  background-color: $red;
  color: white;
  border-radius: 27px;
}
</style>
