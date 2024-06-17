<template>
  <header class="nav-bar_container">
    <nav class="nav-bar">
      <div class="left">
        <MyNavLeft />
      </div>
      <div class="right">
        <MyNavRight />
      </div>
    </nav>
  </header>
</template>

<script setup>
import MyNavLeft from "../components/nav/MyNavLeft.vue";
import MyNavRight from "../components/nav/MyNavRight.vue";
</script>

<style lang="scss">
.nav-bar_container {
  width: 100%;
  min-height: 60px;
  background-color: var(--c-black);
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-bar {
  max-width: 1170px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 2px;
  flex-wrap: wrap;
}

.left,
.right {
  display: flex;
  align-items: center;
}

.left {
  margin-left: 10px;
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
  .left {
    flex-direction: column;
  }
}
</style>
