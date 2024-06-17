<template>
  <input
    type="text"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>

<script setup>
defineProps({
  modelValue: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.input {
  border: 1px solid var(--c-gray);
  border-radius: 5px;
  outline: none;
  font-size: 18px;
  padding-left: 10px;
}

.car-number {
  width: 320px;
  height: 40px;
}

.region {
  width: 213px;
  height: 40px;
}

.reg-cert {
  width: 563px;
  height: 40px;
}

.car-number:focus,
.region:focus,
.reg-cert:focus {
  border: 1px solid var(--c-blue);
}

@media (max-width: 650px) {
  .input {
    max-width: 300px;
  }
}
</style>
