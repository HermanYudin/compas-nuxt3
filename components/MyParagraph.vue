<template>
  <p :class="$attrs.class">{{ p }}</p>
</template>

<script setup>
defineProps({
  p: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.contract_p,
.pers_p,
.pay_p {
  font-size: inherit;
  margin-left: 7px;
  letter-spacing: 0.9px;
  line-height: 22px;
  margin-bottom: 0px;
}

.second {
  margin-top: -4px;
}
</style>
