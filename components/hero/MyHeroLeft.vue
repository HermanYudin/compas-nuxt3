<template>
  <MyVideoOverlay v-if="openedVideo" @close-video="closeVideo" />
  <MyVideo v-if="openedVideo" @close-video="closeVideo" />
  <div class="hero-left">
    <MySectionTitle
      class="hero-title"
      :sectionTitle="'Проверьте штрафы и зарегестрируйтесь в 1 клик'"
    />
    <form class="hero-form" @submit.prevent>
      <div class="hero-form_container">
        <div class="car-number_container">
          <MyInputTitle class="input-title" :inputTitle="'Номер автомобиля'" />
          <MyInput
            class="input car-number"
            :modelValue="carNumber"
            :class="{ 'input-error': error }"
            @update:modelValue="carNumber = $event"
          />
        </div>
        <div class="region_container">
          <MyInputTitle class="input-title" :inputTitle="'Регион'" />
          <MyInput
            class="input region"
            :modelValue="region"
            :class="{ 'input-error': error }"
            @update:modelValue="region = $event"
          />
        </div>
        <div class="reg-cert_container">
          <MyInputTitle
            class="input-title"
            :inputTitle="'Свидетельство о регистрации ТС'"
          />
          <MyInput
            class="input reg-cert"
            :modelValue="regCert"
            :class="{ 'input-error': error }"
            @update:modelValue="regCert = $event"
          />
        </div>
      </div>
      <span class="error" v-if="error"
        >Ошибка! Проверьте правильность заполнения формы</span
      >
      <div class="hero-btns">
        <MyBtn
          class="check-btn"
          :btnTitle="'Проверить штрафы'"
          @click="submitForm()"
        />
        <NuxtLink class="play-btn" @click="openVideo()">
          <span style="color: black">О сервисе &nbsp</span>
          <span style="color: blue; letter-spacing: -0.5px">
            (1 мин. 20 сек)</span
          >
        </NuxtLink>
      </div>
      <MyInputTitle
        class="input-title disc"
        :inputTitle="'Нажимая «Проверить штрафы» вы соглашаетесь с политикой обработки персональных данных и принимаете оферту'"
      />
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";
import MySectionTitle from "../MySectionTitle";
import MyInputTitle from "../MyInputTitle";
import MyInput from "../MyInput";
import MyBtn from "../MyBtn";
import MyVideo from "../video/MyVideo";
import MyVideoOverlay from "../video/MyVideoOverlay";

const carNumber = ref("");
const region = ref("");
const regCert = ref("");
let error = ref(false);
let openedVideo = ref(false);

function submitForm() {
  if (carNumber.value !== "" && region.value !== "" && regCert.value !== "") {
    alert("Данные были отправлены");
    carNumber.value = "";
    region.value = "";
    regCert.value = "";
    error.value = false;
  } else {
    error.value = true;
  }
}

function openVideo() {
  openedVideo.value = true;
}

function closeVideo() {
  openedVideo.value = false;
}
</script>

<style lang="scss" scoped>
.hero-form_container {
  display: flex;
  flex-wrap: wrap;
}

.car-number_container {
  margin-right: 30px;
}

.hero-btns {
  margin-top: 14px;
  margin-left: 0px;
  display: flex;
  flex-wrap: wrap;
}

.error {
  display: inline-block;
  margin-top: 10px;
  color: var(--c-red);
}

.input-error {
  border-color: var(--c-red);
}

@media (max-width: 1200px) {
  .hero-form_container {
    display: block;
  }

  .hero-left {
    margin-left: 10px;
  }
}

@media (max-width: 540px) {
  .play-btn {
    margin-top: 15px;
  }
}
</style>
