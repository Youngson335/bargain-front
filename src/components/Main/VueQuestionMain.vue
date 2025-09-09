<template>
  <div class="vue-question-main block-radius">
    <div class="vue-question-main__title">
      <h3>ваши вопросы -</h3>
      <vue-label class="vue-question-main__title-label">наши ответы</vue-label>
    </div>
    <div class="vue-question-content">
      <div v-for="item of accordion" style="width: 100%">
        <vue-accordion :answer="item.answer" :question="item.question" />
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import VueLabel from "../Label/VueLabel.vue";
import VueAccordion from "../Accordion/VueAccordion.vue";
import type { AccordionProps } from "../Accordion/VueAccordion.vue";

const accordion: AccordionProps[] = [
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
  {
    question: "Внезапно, многие известные личности?",
    answer:
      "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
  },
];
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-question {
  &-main {
    background-color: $white;
    padding: 20px;
    &__title {
      display: flex;
      flex-direction: column;
      justify-content: center;
      width: 100%;
      margin: 0 auto;
      max-width: 500px;
      margin-bottom: 30px;
      & h3 {
        font-size: 45px;
        font-weight: 500;
        text-align: start;
      }
      &-label {
        display: flex;
        justify-content: end;
      }
    }
  }
  &-content {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: 100%;
  }
}
</style>
