<template>
  <main class="main">
    <section class="hero">
      <MyHeroLeft />
      <MyHeroRight />
    </section>
    <section class="pluses">
      <MySectionTitle
        class="pluses-title"
        :sectionTitle="'Плюсы использования сервиса «Компас» для анализа штрафов'"
      />
      <div class="pluses-container">
        <MyPlus v-for="plus in pluses" :key="plus.plusId" :plus="plus" />
      </div>
    </section>
    <section class="slider">
      <MySlider />
    </section>
  </main>
</template>

<script setup>
import MyHeroLeft from "../components/hero/MyHeroLeft.vue";
import MyHeroRight from "../components/hero/MyHeroRight.vue";
import MySectionTitle from "../components/MySectionTitle";
import MyPlus from "../components/pluses/MyPlus";
import MySlider from "./MySlider";
const pluses = [
  {
    plusId: 1,
    plusImg: "/svg/d1.svg",
    plusTitle: "Неограниченый автопарк",
    plusDisc: "Можно добавить неограниченное кол-во машин и водителей",
  },
  {
    plusId: 2,
    plusImg: "/svg/d2.svg",
    plusTitle: "Сокращение затрат до 50%",
    plusDisc:
      "Максимально быстро узнаете о штрафах в автоматическом режиме, тем самым у вас есть время оплатить по скидке",
  },
  {
    plusId: 3,
    plusImg: "/svg/d3.svg",
    plusTitle: "Безопасность",
    plusDisc:
      "Данные передаются в зашифрованном виде, они доступны только получателю",
  },
  {
    plusId: 4,
    plusImg: "/svg/d4.svg",
    plusTitle: "Уведомление о погашении",
    plusDisc:
      "Мы оповестим вас о том, что штраф был погашен и соответствующая запись создана в ГИС ГМП",
  },
  {
    plusId: 5,
    plusImg: "/svg/d5.svg",
    plusTitle: "Квитанция об оплате",
    plusDisc:
      "После совершения оплаты банковской картой на Вашу электронную почту придет квитанция об успешной оплате.",
  },
  {
    plusId: 6,
    plusImg: "/svg/d6.svg",
    plusTitle: "Все история сохраняется по каждой машине",
    plusDisc:
      "Вся история штрафов сохраняется по машине и водителю, позволяет анализировать статистику по штрафам",
  },
];
</script>

<style lang="scss" scoped>
.main {
  max-width: 1170px;
  width: 100%;
  margin: 0 auto;
}

.hero {
  display: flex;
  justify-content: space-between;
  margin-top: 45px;
  margin-left: 10px;
  margin-right: 24px;
}

.pluses {
  margin-top: 95px;
}

.pluses-container {
  display: flex;
  flex-wrap: wrap;
  gap: 37px;
  margin-left: 10px;
  margin-top: 35px;
  border-radius: 10px;
}


@media (max-width: 1200px) {
  .hero {
    flex-wrap: wrap;
    justify-content: center;
  }
}

@media (max-width: 700px) {
  .nav-bar {
    justify-content: center;
    margin: 0px 10px;
  }

  .right,
  .left {
    flex-wrap: wrap;
    justify-content: center;
  }
}

@media (max-width: 400px) {
  .nav-links {
    padding-left: 0px;
  }

  .left {
    flex-direction: column;
  }

  .pluses-container {
    margin-right: 10px;
  }

  .hero {
    margin-left: 24px;
  }
}
</style>
