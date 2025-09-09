<template>
  <div class="vue-accordion" @click="onOpenAnswer">
    <div class="vue-accordion__question">
      <p>{{ props.question }}</p>
      <img :src="plus" alt="" v-if="!isOpenAnswer" />
      <p v-if="isOpenAnswer">скрыть</p>
    </div>

    <p v-if="isOpenAnswer" class="vue-accordion__answer">{{ props.answer }}</p>
  </div>
</template>
<script lang="ts" setup>
import { defineProps, ref } from "vue";
import { plus } from "../../assets/icons";

export interface AccordionProps {
  question: string;
  answer: string;
}

const isOpenAnswer = ref(false);

const onOpenAnswer = () => {
  isOpenAnswer.value = !isOpenAnswer.value;
};

const props = defineProps<AccordionProps>();
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-accordion {
  margin-bottom: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;
  background-color: $gray;
  padding: 10px;
  border-radius: 30px;
  width: 100%;
  cursor: pointer;
  transition: all 0.3s ease;
  &:active {
    scale: 1.02;
    transition: all 0.3s ease;
  }
  &__question {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    background-color: $white;
    padding: 18px;
    border-radius: 60px;
  }
  & img {
    display: block;
  }
  &__answer {
    padding: 18px;
  }
}
</style>
