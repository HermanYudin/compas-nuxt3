<template>
  <div class="modal-container">
    <h2 :class="$attrs.class">{{ modalTitle }}</h2>
  </div>
</template>

<script setup>
defineProps({
  modalTitle: {
    type: String,
  },
});
</script>

<style lang="scss" scoped>
.modal-title {
  font-size: 25px;
  font-weight: bold;
}
</style>
