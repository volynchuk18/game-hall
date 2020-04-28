<template>
  <div class="game-item">
    <div class="featured">Featured</div>
    <img class="game-item-image" src="../../../public/images/game-image.png">
  </div>
</template>

<script>
  export default {
    name: "GameItem"
  }
</script>

<style scoped lang="scss">
  .game-item {
    height: 100%;
    position: relative;
    border-radius: 10px;
    font-weight: bold;
  }

  .featured {
    position: absolute;
    left: 0;
    top: 12px;
    display: flex;
    padding: 6px 8px 6px 6px;
    align-items: center;
    color: #FFFFFF;
    font-size: 12px;
    background: #61C200;
    border-radius: 0 24px 24px 0;
    @media screen and (max-width: 768px) {
      top: 9px;
      font-size: 9px;
      padding: 3px 5px 3px 3px;
    }
  }

  .game-item-image {
    width: 100%;
    height: 100%;
  }
</style>
