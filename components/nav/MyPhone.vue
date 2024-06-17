<template>
  <div>
    <a class="phone_link" href="tel:+74951184422"
      ><span class="phone">{{ phone }}</span></a
    >
  </div>
</template>

<script setup>
const phone = " +7 495 118-44-22";
</script>

<style lang="scss" scoped>
.phone {
  color: var(--c-white);
  font-weight: bold;
  font-size: 18px;
  transition: all 0.3s ease-in-out;
}

.phone:hover {
  color: var(--c-blue);
}

.phone_link {
  text-decoration: none;
}
</style>
