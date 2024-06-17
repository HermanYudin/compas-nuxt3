<template>
  <div class="plus-container">
    <img class="plus-img" :src="plus.plusImg" alt="docsImg" />
    <div class="plus-text-content" :data-index="plus.plusId">
      <h3 class="plus-title" :data-index="plus.plusId">{{ plus.plusTitle }}</h3>
      <p class="plus-disc" :data-index="plus.plusId">{{ plus.plusDisc }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  plus: {
    type: Object,
  },
});
</script>

<style lang="scss" scoped>
.plus-container {
  display: flex;
  align-items: center;
  width: 360px;
  background-color: var(--c-lightgray);
  border: 1px solid var(--c-gray);
  border-radius: 10px;
  margin: 0 auto;
  padding-bottom: 2px;
}

.plus-text-content {
  margin-left: 15px;
}

.plus-img {
  margin-left: 18px;
  max-width: 59px;
}

.plus-title {
  font-size: 17px;
  color: var(--c-blue);
  margin-top: 20px;
  margin-bottom: 0px;
}

.plus-disc {
  font-size: 15px;
  max-width: 250px;
  margin-top: 9px;
}

.plus-disc:nth-child(5) {
  margin-left: 20px;
}

.plus-text-content[data-index="5"],
.plus-text-content[data-index="3"] {
  margin-left: 20px;
}

.plus-disc[data-index="1"],
.plus-disc[data-index="2"],
.plus-disc[data-index="3"] {
  margin-top: 10px;
}

.plus-title[data-index="4"],
.plus-title[data-index="5"],
.plus-title[data-index="6"] {
  margin-top: 25px;
}
</style>
