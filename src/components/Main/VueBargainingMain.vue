<template>
  <div class="vue-bargaining-main">
    <div class="vue-bargaining-main__header">
      <h2>Стоимость участия в торгах</h2>
      <vue-label>"под ключ"</vue-label>
    </div>
    <div class="vue-bargaining-main__main">
      <img :src="grafic" alt="" />
    </div>
    <div class="vue-bargaining-main__footer block-radius">
      <div class="vue-bargaining-main__footer-info">
        <vue-icon :image="minus" />
        <p>
          Расскажем что делать, чтобы было меньше шансов попасть в РНП или
          потерять деньги
        </p>
      </div>
      <vue-button :color="'red'">получить консультацию</vue-button>
    </div>
  </div>
</template>
<script lang="ts" setup>
import VueLabel from "../Label/VueLabel.vue";
import { grafic } from "../../assets/images";
import { minus } from "../../assets/icons";
import VueIcon from "../Icon/VueIcon.vue";
import VueButton from "../Button/VueButton.vue";
</script>
<style lang="scss">
@import "../../assets/scss/color.scss";
.vue-bargaining-main {
  &__header {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 50px;
    & h2 {
      font-weight: 400;
      font-size: 40px;
    }
  }
  &__main {
    margin-bottom: 20px;
    & img {
      display: block;
      width: 100%;
    }
  }
  &__footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: $white;
    padding: 20px;
    &-info {
      display: flex;
      gap: 20px;
      align-items: center;
      & p {
        max-width: 500px;
        font-weight: 600;
      }
    }
  }
}
</style>
