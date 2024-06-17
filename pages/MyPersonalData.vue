<template>
  <div class="pers-disc">
    <ul class="pers-links">
      <li class="pers-item" v-for="(link, index) in persLinks" :key="index">
        <NuxtLink
          class="pers-link"
          :data-index="index"
          :to="{
            name:
              link === 'Главная страница'
                ? 'index'
                : link === 'Документы'
                ? 'MySlider'
                : 'MyPersonalData',
          }"
        >
          {{ link }}
        </NuxtLink>
      </li>
    </ul>
    <MySectionTitle
      class="pers-title"
      sectionTitle="Политика обработки персональных данных"
    />
    <MySectionTitle class="pers_past-title" sectionTitle="Заголовок 2" />
    <MyParagraph
      class="pers_p"
      :p="'Представленная тележка-дозатор обеспечивает высококачественную обработку любых территорий сыпучими противогололедными реагентами самых разных типов, включая такие тяжелые, как гранитная и мраморная крошка, песок и пескосоляные смеси. '"
    />
  </div>
</template>

<script setup>
import MySectionTitle from "../components/MySectionTitle";
import MyParagraph from "../components/MyParagraph";

const route = useRoute();
const persLinks = [
  "Главная страница",
  "Документы",
  "Политика обработки персональных данных",
];
</script>

<style lang="scss" scoped>
.pers-disc {
  max-width: 1170px;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  margin-top: 20px;
}

.pers-links {
  display: flex;
  gap: 26px;
  font-size: 13px;
  padding-left: 10px;
  margin-top: 0px;
}

.pers-link {
  text-decoration: none;
  color: var(--c-black);
  cursor: pointer;
}

.pers-item:nth-child(1) {
  list-style-type: none;
}

.pers-link[data-index="2"] {
  color: var(--c-gray);
}
</style>
