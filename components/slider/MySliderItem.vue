<template>
  <div class="slider-item">
    <div class="slider-text-content" :data-index="sliderItem.itemId">
      <h2 class="slider-item_title">{{ sliderItem.itemTitle }}</h2>
      <p class="slider-item_disc" :data-index="sliderItem.itemId">
        {{ sliderItem.itemDisc }}
      </p>
    </div>
    <NuxtLink class="sliderBtn_link" :to="sliderItem.itemLink"
      ><MyBtn class="sliderBtn" :btnTitle="'Перейти'"
    /></NuxtLink>
  </div>
</template>

<script setup>
import MyBtn from "../MyBtn";
defineProps({
  sliderItem: {
    type: Object,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.slider-item {
  display: flex;
  flex-direction: column;
  min-height: 424px;
}

.slider-text-content {
  margin-left: 25px;
  flex-grow: 1;
}

.slider-item_title {
  font-size: 31px;
  color: var(--c-blue);
  font-weight: bold;
  line-height: 37px;
  max-width: 300px;
  margin-bottom: 0px;
}

.slider-item_disc {
  max-width: 292px;
  letter-spacing: 1px;
}

.slider-item_disc[data-index="2"] {
  margin-top: 10px;
}

.sliderBtn_link {
  text-decoration: none;
}
</style>
