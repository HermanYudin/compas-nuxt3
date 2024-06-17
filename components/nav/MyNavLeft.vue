<template>
  <NuxtLink :to="'/'"><MyLogo class="logo" /></NuxtLink>
  <ul class="nav-links">
    <li class="nav-link" v-for="(link, index) in links" :key="index">
      <NuxtLink
        class="nav-link"
        :to="{ name: link === 'Тарифы' ? 'MyRates' : 'MyContacts' }"
      >
        {{ link }}
      </NuxtLink>
    </li>
  </ul>
</template>

<script setup>
import MyLogo from "./MyLogo";

const route = useRoute();
const links = ["Тарифы", "Контакты"];
</script>

<style lang="scss" scoped>
.nav-links {
  display: flex;
  gap: 30px;
  padding-left: 30px;
}

.nav-link {
  list-style-type: none;
  color: var(--c-white);
  font-size: 18px;
  cursor: pointer;
  text-decoration: none;
  transition: all 0.3s ease-in-out;
}

.nav-link:hover {
  color: var(--c-blue);
}

@media (max-width: 400px) {
  .nav-links {
    padding-left: 0px;
  }

  .logo {
    margin-top: 10px;
  }
}
</style>
