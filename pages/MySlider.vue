<template>
  <section class="slider" id="slider" >
    <MySectionTitle class="slider-title" :sectionTitle="'Документы'" />
    <Swiper
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :spaceBetween="35"
      :breakpoints="{
        1: {
          slidesPerView: 1,
          slidesPerGroup: 1,
        },
        381: {
          slidesPerView: 1,
          slidesPerGroup: 1,
        },
        900: {
          slidesPerView: 2,
          slidesPerGroup: 2,
        },
        1200: {
          slidesPerView: 3,
          slidesPerGroup: 3,
        },
        1500: {
          slidesPerView: 3,
          slidesPerGroup: 3,
        },
      }"
      ,
      class="mySwiper"
    >
      <SwiperSlide v-for="sliderItem in sliderItems" :key="sliderItem.itemId">
        <MySliderItem :sliderItem="sliderItem" />
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup>
import MySliderItem from "../components/slider/MySliderItem";

import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.min.css";
import "swiper/components/navigation/navigation.min.css";

// import Swiper core and required modules
import SwiperCore, { Pagination, Navigation } from "swiper/core";

SwiperCore.use([Pagination, Navigation]);

const sliderItems = [
  {
    itemId: 1,
    itemTitle: "Лицензионный договор",
    itemDisc:
      "Механизм разбрасывания веерного типа приводится в действие от колес тележки, отличается простой и надежной конструкцией, не нуждается в смазке. ",
    itemLink: "./MyContract",
  },
  {
    itemId: 2,
    itemTitle: "Политика обработки персональных данных",
    itemDisc:
      "Радиус разброса ПГМ составляет до 3 метров и может регулироваться. ",
    itemLink: "./MyPersonalData",
  },
  {
    itemId: 3,
    itemTitle: "Информация об оплате",
    itemDisc:
      "Десятипозиционный переключатель дозировки расположен на ручке тележки и позволяет очень точно регулировать объем рассыпаемого реагента с учетом его массы и фракции.",
    itemLink: "./MyPayInfo",
  },
  {
    itemId: 4,
    itemTitle: "Лицензионный договор 2",
    itemDisc:
      "Механизм разбрасывания веерного типа приводится в действие от колес тележки, отличается простой и надежной конструкцией, не нуждается в смазке. ",
    itemLink: "./MyContract",
  },
  {
    itemId: 5,
    itemTitle: "Политика обработки персональных данных 2",
    itemDisc:
      "Радиус разброса ПГМ составляет до 3 метров и может регулироваться. ",
    itemLink: "./MyPersonalData",
  },
  {
    itemId: 6,
    itemTitle: "Информация об оплате 2",
    itemDisc:
      "Десятипозиционный переключатель дозировки расположен на ручке тележки и позволяет очень точно регулировать объем рассыпаемого реагента с учетом его массы и фракции.",
    itemLink: "./MyPayInfo",
  },
];
</script>

<style lang="scss" scoped>
.slider {
  margin-left: 13px;
  padding-bottom: 100px;
}

.swiper-container {
  margin: 0 auto;
  padding-top: 14px;
  padding-left: 32px;
  max-width: 1147px;
}

.swiper-wrapper {
  padding-bottom: 39px;
}

.swiper-slide,
.swiper-slide-active {
  background-color: var(--c-white);
  border-radius: 10px;
  box-shadow: 0px 0px 25px -5px var(--c-gray);
  display: flex;
  flex-direction: column;
  padding-bottom: 23px;
  max-width: 340px;
}

.slider-text-content {
  margin-left: 25px;
  padding-bottom: 122px;
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
  margin-left: 4px;
}

@media (max-width: 1200px) {
  .swiper-container {
    padding-left: 10px;
    padding-right: 10px;
    margin-left: 0px;
    max-width: 680px;
    margin: 0 auto;
  }
}

@media (max-width: 950px) {
  .swiper-container {
    padding-left: 10px;
    padding-right: 10px;
    margin-left: 0px;
    max-width: 680px;
    margin: 0 auto;
  }
}

@media (max-width: 900px) {
  .swiper-container {
    max-width: 340px;
  }

  .slider {
    margin-left: 0px;
  }
}

@media (min-width: 905px) {
  .swiper-button-next,
  .swiper-button-prev {
    display: none;
  }
}
</style>
