<template>
  <div class="vue-main container">
    <vue-bargaining-main class="vue-main-block" />
    <vue-description-main class="vue-main-block" />
    <vue-question-main />
  </div>
</template>
<script lang="ts" setup>
import VueBargainingMain from "./VueBargainingMain.vue";
import VueDescriptionMain from "./VueDescriptionMain.vue";
import VueQuestionMain from "./VueQuestionMain.vue";
</script>
<style lang="scss">
.vue-main {
  &-block {
    margin-bottom: 20px;
  }
}
</style>
