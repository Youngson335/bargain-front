<template>
  <div class="vue-services-form block-radius">
    <div class="vue-services-form__title">
      <h3>Рассчитайте стоимость наших услуг прямо сейчас</h3>
    </div>
    <div class="vue-services-form__inputs">
      <vue-text-input v-model="userName" :placeholder="'ваше имя'" />
      <vue-text-input v-model="userPhone" :placeholder="'ваш телефон'" />
    </div>
    <div class="vue-services-form__action">
      <vue-button :color="'red'"> получить консультацию </vue-button>
      <p>Нажимая на кнопку, я соглашаюсь с политикой конфиденциальности</p>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { ref } from "vue";
import VueTextInput from "../Input/VueTextInput.vue";
import VueButton from "../Button/VueButton.vue";

const userName = ref("");
const userPhone = ref("");
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-services-form {
  background-color: $gray;
  padding: 20px;
  &__title {
    & h3 {
      font-weight: 600 !important;
      font-size: 20px !important;
      line-height: 22px !important;
    }
  }
  &__inputs {
    display: flex;
    flex-direction: column;
    gap: 5px;
    margin-bottom: 10px;
  }
  &__action {
    display: flex;
    flex-direction: column;
    justify-content: center;
    & p {
      font-size: 10px;
      text-align: center;
      line-height: 10px;
    }
    & button {
      margin-bottom: 5px;
    }
  }
}
</style>
