<template>
  <div class="overlay" @click="$emit('closeVideo')"></div>
</template>

<script setup></script>

<style lang="scss" scoped>
.overlay {
  background-color: var(--c-black);
  z-index: 2;
  position: fixed;
  opacity: 0.3;
}
</style>
