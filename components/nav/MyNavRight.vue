<template>
  <div class="right-container">
    <MyPhone class="phone" />
    <div class="btns">
      <NuxtLink :to="'MyEnterPage'"
        ><MyBtn class="enter-btn" :btnTitle="'Вход'"
      /></NuxtLink>
      <NuxtLink :to="'MyRegPage'"
        ><MyBtn class="reg-btn" :btnTitle="'Регистрация'"
      /></NuxtLink>
    </div>
  </div>
</template>

<script setup>
import MyPhone from "./MyPhone";
import MyBtn from "../MyBtn";
</script>

<style lang="scss" scoped>
.btns,
.right-container {
  display: flex;
  align-items: center;
}

.phone {
  margin-right: 25px;
}

@media (max-width: 1200px) {
  .reg-btn {
    margin-right: 15px;
  }
}

@media (max-width: 700px) {
  .btns {
    margin-bottom: 10px;
  }
}

@media (max-width: 400px) {
  .right-container {
    flex-wrap: wrap;
    justify-content: center;
  }

  .btns {
    margin-top: 15px;
    margin-left: 30px;
  }
}
</style>
