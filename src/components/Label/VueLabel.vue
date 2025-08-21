<template>
  <div class="vue-label">
    <label class="vue-label--label block-radius">
      <slot />
    </label>
  </div>
</template>
<script lang="ts" setup></script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-label {
  &--label {
    font-size: 45px;
    color: $white;
    background-color: $red;
    padding: 15px;
  }
}
</style>
