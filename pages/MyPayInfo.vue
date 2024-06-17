<template>
  <div class="pay-disc">
    <ul class="pay-links">
      <li class="pay-item" v-for="(link, index) in payLinks" :key="index">
        <NuxtLink
          class="pay-link"
          :data-index="index"
          :to="{
            name:
              link === 'Главная страница'
                ? 'index'
                : link === 'Документы'
                ? 'MySlider'
                : 'MyPayInfo',
          }"
        >
          {{ link }}
        </NuxtLink>
      </li>
    </ul>
    <MySectionTitle class="pay-title" sectionTitle="Информация об оплате" />
    <MySectionTitle class="pay_past-title" sectionTitle="Заголовок 3" />
    <MyParagraph
      class="pay_p"
      :p="'Представленная тележка-дозатор обеспечивает высококачественную обработку любых территорий сыпучими противогололедными реагентами самых разных типов, включая такие тяжелые, как гранитная и мраморная крошка, песок и пескосоляные смеси. Тележка прекрасно подходит для использования во дворах многоквартирных домов, обработки территорий промышленных предприятий, востребована владельцами магазинов, различных коммерческих компаний. Кроме того, она может использоваться для высева семян на газонах, теннисных кортах и других территориях.'"
    />
    <br />
    <MyParagraph
      class="pay_p second"
      :p="'Представленная тележка-дозатор обеспечивает высококачественную обработку любых территорий сыпучими противогололедными реагентами самых разных типов, включая такие тяжелые, как гранитная и мраморная крошка, песок и пескосоляные смеси.'"
    />
  </div>
</template>

<script setup>
import MySectionTitle from "../components/MySectionTitle";
import MyParagraph from "../components/MyParagraph";

const route = useRoute();
const payLinks = ["Главная страница", "Документы", "Информация об оплате"];
</script>

<style lang="scss" scoped>
.pay-disc {
  max-width: 1170px;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  margin-top: 20px;
}

.pay-links {
  display: flex;
  gap: 26px;
  font-size: 13px;
  padding-left: 10px;
  margin-top: 0px;
}

.pay-link {
  text-decoration: none;
  color: var(--c-black);
  cursor: pointer;
}

.pay-item:nth-child(1) {
  list-style-type: none;
}

.pay-link[data-index="2"] {
  color: var(--c-gray);
}
</style>
