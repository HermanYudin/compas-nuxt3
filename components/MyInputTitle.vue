<template>
  <div>
    <h2 :class="$attrs.class">{{ inputTitle }}</h2>
  </div>
</template>

<script setup>
defineProps({
  inputTitle: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.input-title {
  font-size: 12px;
  font-weight: normal;
  margin-bottom: 6px;
  margin-top: 12px;
}

.disc {
  margin-top: 15px;
  max-width: 560px;
  letter-spacing: 0.5px;
  color: var(--c-gray);
}
</style>
