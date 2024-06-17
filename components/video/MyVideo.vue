<template>
  <div class="video-container">
    <div class="close-container" @click="$emit('closeVideo')">
      <img class="close" :src="close" alt="close" />
    </div>
    <iframe
      class="video"
      src="https://www.youtube.com/embed/WkBX4N79r4w?si=-uPhEouxgebSeJVJ"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      referrerpolicy="strict-origin-when-cross-origin"
      allowfullscreen
    ></iframe>
  </div>
</template>

<script setup>
const close = "/svg/close.svg";
</script>

<style lang="scss" scoped>
.video-container {
  position: fixed;
  max-width: 960px;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center;
  z-index: 3;
}

.video {
  width: 960px;
  min-height: 532px;
}

.close-container {
  position: absolute;
  right: 0;
  top: -25px;
  cursor: pointer;
}

@media (max-width: 1000px) {
  .video-container {
    max-width: 700px;
  }

  .video {
    max-width: 700px;
    min-height: 532px;
  }
}

@media (max-width: 750px) {
  .video-container {
    max-width: 500px;
  }

  .video {
    max-width: 500px;
    min-height: 432px;
  }
}

@media (max-width: 550px) {
  .video-container {
    width: 330px;
  }

  .video {
    width: 330px;
  }
}
</style>
