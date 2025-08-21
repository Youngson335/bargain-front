<template>
  <div class="vue-description-main">
    <div class="vue-description-main__block">
      <div class="vue-description-main__block-image">
        <img :src="people_2" alt="" />
      </div>
      <div>
        <h3>Для многих гос. закупки — сложно, но всё может быть иначе</h3>
        <div class="vue-description-main__block-title">
          <vue-icon :image="user" />
          <p>Внезапно, многие известные</p>
        </div>
        <div class="vue-description-main__block-description">
          <p>
            Внезапно, многие известные личности, инициированные исключительно
            синтетически, ассоциативно распределены по отраслям. Разнообразный и
            богатый опыт говорит нам, что перспективное планирование
            обеспечивает широкому кругу (специалистов) участие в формировании
            направлений прогрессивного развития. Ясность нашей позиции очевидна:
            высокотехнологичная концепция общественного уклада однозначно
            фиксирует необходимость благоприятных перспектив.
          </p>
        </div>
      </div>
    </div>

    <div class="vue-description-main__block">
      <div>
        <div class="vue-description-main__block-title">
          <vue-icon :image="check" />
          <p>Внезапно, многие известные</p>
        </div>
        <p class="vue-description-main__block-description">
          формировании направлений прогрессивного развития. Ясность нашей
          позиции очевидна: высокотехнологичная концепция общественного уклада
          однозначно фиксирует необходимость
        </p>
      </div>
      <div>
        <img :src="work" alt="" />
      </div>
      <vue-services-form />
    </div>
  </div>
</template>
<script lang="ts" setup>
import { people_2, work } from "../../assets/images";
import { user, check } from "../../assets/icons";
import VueIcon from "../Icon/VueIcon.vue";
import VueServicesForm from "../Form/VueServicesForm.vue";
</script>
<style lang="scss">
.vue-description-main {
  &__block {
    display: flex;
    gap: 5%;
    margin-bottom: 20px;
    &-image {
      display: block;
      width: 100%;
      min-width: 350px;
      & img {
        width: 100%;
      }
    }
    & h3 {
      font-weight: 400;
      font-size: 35px;
      margin-bottom: 20px;
    }
    &-title {
      display: flex;
      align-items: center;
      gap: 5%;
      margin-bottom: 20px;
      & p {
        font-size: 20px;
        max-width: 250px;
      }
    }
    &-description {
      font-size: 13px;
      max-width: 400px;
    }
  }
}
</style>
