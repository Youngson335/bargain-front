<template>
  <div class="vue-content-header block-radius">
    <div class="vue-content-header-info">
      <div class="vue-content-header-info__description">
        <p>Работа с нами – это минимальные риски и максимальная прибыль</p>
        <h2>Находим госзакупки и выигрываем торги!</h2>
      </div>
      <div class="vue-content-header-info__cards">
        <vue-advantage-card :advantage-data="advantageDataLike" />
        <vue-advantage-card :advantage-data="advantageDataSearch" />
      </div>
      <div class="vue-content-header-info__action">
        <vue-button :color="'red'"> подробнее </vue-button>
        <p>Заработать с нами на госзаказах – это просто</p>
      </div>
    </div>

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
import VueAdvantageCard from "../Cards/VueAdvantageCard.vue";
import type AdvantageData from "../Cards/AdvantageData";
import { ref } from "vue";
import { like, search } from "../../assets/icons";
import VueButton from "../Button/VueButton.vue";

const userName = ref("");
const userPhone = ref("");

const advantageDataLike: AdvantageData = {
  image: like,
  text: "Мы работаем по госзаказам с минимальными рисками и максимальной прибылью",
};
const advantageDataSearch: AdvantageData = {
  image: search,
  text: "Подход к работе выработанна основе анализа полученного опыта",
};
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
    padding: 25px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: start;
    gap: 15px;
    &__description {
      & p {
        font-weight: 500;
        font-size: 13px;
        line-height: 16px;
      }
      & h2 {
        font-weight: 500;
        font-size: 40px;
        line-height: 48px;
      }
    }
    &__cards {
      display: flex;
      flex-direction: column;
      gap: 5px;
    }
    &__action {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
      & p {
        font-weight: 600;
        font-size: 13px;
        line-height: 16px;
        max-width: 200px;
      }
    }
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
