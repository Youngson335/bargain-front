<template>
  <div class="vue-question-main">
    <div class="vue-question-main__title">
      <h3>ваши вопросы -</h3>
      <vue-label class="vue-question-main__title-label">наши ответы</vue-label>
    </div>
    <div>
      <vue-accordion
        :answer="accordion.answer"
        :question="accordion.question"
      />
    </div>
  </div>
</template>
<script lang="ts" setup>
import VueLabel from "../Label/VueLabel.vue";
import VueAccordion from "../Accordion/VueAccordion.vue";
import type { AccordionProps } from "../Accordion/VueAccordion.vue";

const accordion: AccordionProps = {
  question: "Внезапно, многие известные личности?",
  answer:
    "формировании направлений прогрессивного развития. Ясность нашей позиции очевидна: высокотехнологичная концепция общественного уклада однозначно фиксирует необходимость общественного уклада однозначно ",
};
</script>
<style lang="scss">
.vue-question-main {
  &__title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    margin: 0 auto;
    max-width: 500px;
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
</style>
