<template>
  <div class="gamehall-background">
    <img src="../../../public/images/gamehall-bg.png">
    <div class="bg-1"></div>
    <div class="bg-2"></div>
  </div>
</template>

<script>
  export default {
    name: "GameHallBackground"
  }
</script>

<style scoped>
  .gamehall-background {
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    width: 100%;
    opacity: 0.7;
  }

  .bg-1 {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(180deg, rgba(17, 15, 54, 0) 0%, #110F36 100%);
  }

  .bg-2 {
    position: absolute;
    top: 0;
    width: 100%;
    height: 100%;
    background: #110F36;
    opacity: 0.7;
  }

  img {
    width: 100%;
  }
</style>
