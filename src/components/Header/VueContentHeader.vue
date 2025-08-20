<template>
  <div class="vue-content-header block-radius">
    <div class="vue-content-header-info"></div>
    <div class="vue-content-header-form block-radius">
      <div class="vue-content-header-form--block block-radius">
        <div class="vue-content-header-form__item">
          <vue-text-input v-model="userName" :placeholder="'Ваше имя'" />
        </div>
        <div class="vue-content-header-form__item">
          <vue-text-input v-model="userPhone" :placeholder="'Ваш телефон'" />
        </div>
        <div
          class="vue-content-header-form__item vue-content-header-form__description"
        >
          <p>Нажимая на кнопку, я соглашаюсь с политикой конфиденциальности</p>
          <vue-border-button>получить консультацию</vue-border-button>
        </div>
      </div>
    </div>
  </div>
</template>
<script lang="ts" setup>
import VueTextInput from "../Input/VueTextInput.vue";
import VueBorderButton from "../Button/VueBorderButton.vue";
import { ref } from "vue";

const userName = ref("");
const userPhone = ref("");
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-content-header {
  height: 500px;
  padding: 10px;
  background-color: $gray;
  display: flex;
  &-info {
    width: 55%;
  }
  &-form {
    width: 45%;
    background-image: url(../../assets/images/people-1.png);
    height: 100%;
    background-position-x: -300px;
    background-size: cover;
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: start;
    padding: 15px;
    &__item {
      width: 100%;
      margin-bottom: 10px;
      & p {
        font-size: 10px;
        line-height: 10px;
        color: $text_black;
        width: 30%;
      }
    }
    &--block {
      backdrop-filter: blur(5px);
      padding: 25px;
    }
    &__description {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 5%;
    }
  }
}
</style>
