<template>
  <button class="vue-button" :class="`vue-button-${props.color}`">
    <slot />
  </button>
</template>
<script lang="ts" setup>
import { defineProps } from "vue";
import ButtonColors from "./ButtonColors";

interface Props {
  color: ButtonColors | string;
}

const props = defineProps<Props>();
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-button {
  padding: 15px 25px;
  border-radius: 27px;
  transition: all 0.4s ease;
  font-weight: 600;
  cursor: pointer;
  border: none;
  &:active {
    scale: 1.05;
    transition: all 0.4s ease;
  }
  &-red {
    background-color: $red;
    color: $white;
  }
  &-white {
    background-color: $white;
    color: $red;
  }
}
</style>
