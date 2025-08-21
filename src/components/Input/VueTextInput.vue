<template>
  <div class="vue-text-input">
    <input
      type="text"
      v-model="internalValue"
      @input="onInput"
      :placeholder="internalPlaceholder"
    />
  </div>
</template>
<script lang="ts" setup>
import { defineProps, ref, defineEmits } from "vue";

const props = defineProps<{
  modelValue: string | number;
  placeholder?: string;
}>();

const emits = defineEmits(["update:modelValue"]);

const internalValue = ref<string | number>(props.modelValue);
const internalPlaceholder = ref<string>(props.placeholder || "");

const onInput = () => {
  emits("update:modelValue", internalValue.value);
};
</script>
<style lang="scss">
input {
  padding: 15px 20px;
  width: 100%;
  border-radius: 50px;
  &::placeholder {
    font-weight: 500;
  }
}

.vue-text-input {
  width: 100%;
}
</style>
