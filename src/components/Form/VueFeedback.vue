<template>
  <div class="vue-feedback">
    <p>Рассчитайте стоимость наших услуг прямо сейчас</p>
    <div class="vue-feedback__input">
      <vue-text-input v-model="userName" :placeholder="'Ваше имя'" />
    </div>
    <div class="vue-feedback__input">
      <vue-text-input v-model="userPhone" :placeholder="'Ваш телефон'" />
    </div>
    <vue-button :color="'red'"> Получить консультацию </vue-button>
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
.vue-feedback {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  &__input {
    max-width: 200px;
  }
  & p {
    max-width: 200px;
  }
}
</style>
