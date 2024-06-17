<template>
  <div class="contract-disc">
    <ul class="contract-links">
      <li
        class="contract-item"
        v-for="(link, index) in contractLinks"
        :key="index"
      >
        <NuxtLink
          class="contract-link"
          :data-index="index"
          :to="{
            name:
              link === 'Главная страница'
                ? 'index'
                : link === 'Документы'
                ? 'MySlider'
                : 'MyContract',
          }"
        >
          {{ link }}
        </NuxtLink>
      </li>
    </ul>
    <MySectionTitle
      class="contract-title"
      sectionTitle="Лицензионный договор"
    />
    <MySectionTitle class="contract_past-title" sectionTitle="Заголовок 1" />
    <MyParagraph
      class="contract_p"
      :p="'Представленная тележка-дозатор обеспечивает высококачественную обработку любых территорий сыпучими противогололедными реагентами самых разных типов, включая такие тяжелые, как гранитная и мраморная крошка, песок и пескосоляные смеси. Тележка прекрасно подходит для использования во дворах многоквартирных домов, обработки территорий промышленных предприятий, востребована владельцами магазинов, различных коммерческих компаний. Кроме того, она может использоваться для высева семян на газонах, теннисных кортах и других территориях.'"
    />
    <br />
    <MyParagraph
      class="contract_p second"
      :p="'Представленная тележка-дозатор обеспечивает высококачественную обработку любых территорий сыпучими противогололедными реагентами самых разных типов, включая такие тяжелые, как гранитная и мраморная крошка, песок и пескосоляные смеси.'"
    />
  </div>
</template>

<script setup>
import MySectionTitle from "../components/MySectionTitle";
import MyParagraph from "../components/MyParagraph";

const route = useRoute();
const contractLinks = ["Главная страница", "Документы", "Лицензионный договор"];
</script>

<style lang="scss" scoped>
.contract-disc {
  max-width: 1170px;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  margin-top: 20px;
}

.contract-links {
  display: flex;
  gap: 26px;
  font-size: 13px;
  padding-left: 10px;
  margin-top: 0px;
}

.contract-link {
  text-decoration: none;
  color: var(--c-black);
  cursor: pointer;
}

.contract-item:nth-child(1) {
  list-style-type: none;
}

.contract-link[data-index="2"] {
  color: var(--c-gray);
}
</style>
