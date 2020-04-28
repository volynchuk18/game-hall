<template>
  <div class="game-achievements">
    <div class="get-achievements-container">
      <div class="game-achievements-header">
        <LabelAchievements />
        <LabelValue crystal :value="0" />
      </div>
      <div class="game-achievements-items-wrapper">
        <div class="game-achievements-items">
          <img class="game-achievements-item" src="/icons/ach-3.png">
          <div class="bonus-item">
            <BonusSmall
              :bonus="2"
            />
            <img class="game-achievements-item" src="/icons/ach-1.png">
          </div>
          <img class="game-achievements-item" src="/icons/ach-2.png">
        </div>
      </div>
      <CustomButton class="get-achievements">
        Get Achievements
      </CustomButton>
    </div>
    <div class="background"></div>
  </div>
</template>

<script>
  import CustomButton from "../common/CustomButton";
  import LabelAchievements from "../common/LabelAchievements";
  import LabelValue from "../common/LabelValue";
  import BonusSmall from "../common/BonusSmall";
  export default {
    name: "GameAchievements",
    components: {BonusSmall, LabelValue, LabelAchievements, CustomButton}
  }
</script>

<style scoped lang="scss">
  .game-achievements {
    position: relative;
    padding: 24px 0 24px;
    border-radius: 10px;
    overflow: hidden;
    background: url("../../../public/images/eldorado-gonzosquest-image.png");
    background-size: 100% 100%;
    font-weight: bold;
  }

  .get-achievements-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    > * {
      z-index: 2;
    }
  }

  .game-achievements-header {
    display: flex;
    justify-content: space-between;
  }

  .game-achievements-items-wrapper {
    width: 100%;
    display: grid;
    align-items: center;
    justify-content: center;
  }

  .game-achievements-items {
    display: flex;
    margin: auto;
  }

  .game-achievements-item {
    width: 140px;
    height: 140px;
    margin: 0 -10px;
  }

  .bonus-item {
    position: relative;
  }

  .bonus-small {
    position: absolute;
    top: 6%;
    left: 0;
    right: 0;
    width: fit-content;
    margin: 0 auto;
  }

  .background {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background: #110F36;
    opacity: 0.4;
    z-index: 1;
  }
</style>
