<template>
  <button class="vue-button" :class="`vue-button-${buttonColor}`">
    <slot />
  </button>
</template>
<script lang="ts" setup>
import { defineProps, computed, withDefaults } from "vue";
import ButtonColors from "./ButtonColors";

interface Props {
  color?: ButtonColors;
}

const props = withDefaults(defineProps<Props>(), {
  color: ButtonColors.WHITE, // Default value for optional 'count' prop
});

const buttonColor = computed((): ButtonColors => {
  return props.color;
});
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";

.vue-button {
  padding: 10px 20px;
  border-radius: 27px;
  transition: all 0.4s ease;
  font-weight: 600;
  cursor: pointer;
  &:active {
    scale: 1.05;
    transition: all 0.4s ease;
  }
  &-red {
    background-color: $red;
    color: $white;
    border: 3px solid $white;
  }
  &-white {
    background-color: $white;
    color: $red;
    border: 3px solid $red;
  }
}
</style>
