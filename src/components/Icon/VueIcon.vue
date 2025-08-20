<template>
  <div class="vue-icon">
    <img :src="props.image" alt="" />
  </div>
</template>
<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps<{
  image: string;
}>();
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-icon {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  background-color: $red;
  padding: 10px;
  border-radius: 20px;
}
</style>
