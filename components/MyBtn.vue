<template>
  <button :class="$attrs.class">
    {{ btnTitle }}
  </button>
</template>

<script setup>
defineProps({
  btnTitle: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss">
.enter-btn,
.reg-btn {
  color: var(--c-white);
  font-size: 18px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.reg-btn:hover {
  background-color: var(--c-white);
  color: var(--c-blue);
}

.enter-btn {
  background-color: transparent;
  border: none;
  margin-right: 23px;
}

.enter-btn:hover {
  color: var(--c-blue);
}

.reg-btn {
  background-color: var(--c-blue);
  padding: 9px 14px;
  font-size: 15px;
  border-radius: 5px;
  border: none;
}

.check-btn {
  background-image: url("../public/svg/arrow.svg");
  background-color: var(--c-blue);
  background-repeat: no-repeat;
  background-position: 90% 19px;
  color: var(--c-white);
  font-size: 18px;
  cursor: pointer;
  border: 1px solid transparent;
  padding: 12px 20px;
  border-radius: 10px;
  letter-spacing: -1px;
  padding-right: 39px;
  margin-right: 20px;
  transition: all 0.3s ease-in-out;
}

.check-btn:hover {
  background-color: var(--c-arrows);
  border: 1px solid var(--c-arrows);
}

.play-btn {
  background-image: url("../public/svg/play.svg");
  background-color: var(--c-white);
  background-repeat: no-repeat;
  border-radius: 5px;
  padding: 12px 21px;
  border-radius: 10px;
  border: 1px solid var(--c-blue);
  padding-bottom: 10px;
  padding-left: 58px;
  background-position: 8% center;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.play-btn:hover {
  background-color: var(--c-arrows);
  border: 1px solid var(--c-arrows);
}

.sliderBtn {
  padding: 11px 108px;
  background-color: var(--c-blue);
  color: var(--c-white);
  border-radius: 10px;
  border: 1px solid transparent;
  margin: 0 auto;
  display: flex;
  font-size: 18px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}

.sliderBtn:hover {
  background-color: var(--c-white);
  color: var(--c-blue);
  border: 1px solid var(--c-blue);
}
</style>
