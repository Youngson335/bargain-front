<template>
  <div class="vue-advantage-card block-radius">
    <vue-icon :image="props.advantageData.image" />
    <p class="vue-advantage-card__text">{{ props.advantageData.text }}</p>
  </div>
</template>
<script lang="ts" setup>
import VueIcon from "../Icon/VueIcon.vue";
import { defineProps } from "vue";
import type AdvantageData from "./AdvantageData";

interface Props {
  advantageData: AdvantageData;
}

const props = defineProps<Props>();
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-advantage-card {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  max-width: 320px;
  padding: 15px;
  background-color: $white;
  &__text {
    font-weight: 600;
    font-size: 15px;
    line-height: 15px;
    color: rgba(0, 27, 27, 0.8);
  }
}
</style>
