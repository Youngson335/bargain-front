<template>
  <div class="vue-accordion">
    <div>
      <div>
        <p>{{ props.question }}</p>
      </div>
      <div>
        <img :src="plus" alt="" />
      </div>
    </div>

    <p v-if="isOpenAnswer">{{ props.answer }}</p>
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

const props = defineProps<AccordionProps>();
</script>
<style lang="scss"></style>
