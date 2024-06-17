<template>
  <h2 :class="$attrs.class">{{ sectionTitle }}</h2>
</template>

<script setup>
defineProps({
  sectionTitle: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.hero-title {
  font-size: 41px;
  font-weight: bold;
  line-height: 50px;
  margin-bottom: 10px;
}

.pluses-title,
.slider-title {
  font-size: 34px;
  text-align: center;
  margin-right: 10px;
}

.slider-title {
  margin-left: 63px;
  margin-top: 31px;
  margin-bottom: 28px;
}

.contract-title,
.pay-title,
.pers-title {
  font-size: 41px;
  margin-left: 10px;
  margin-top: 4px;
}

.contract_past-title,
.pers_past-title,
.pay_past-title {
  font-size: 41px;
  margin-top: 2px;
  margin-left: 10px;
  margin-bottom: 7px;
}

@media (max-width: 550px) {
  .hero-title {
    font-size: 32px;
  }
}
</style>
