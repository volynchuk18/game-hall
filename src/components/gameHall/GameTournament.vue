<template>
  <div class="game-tournament">
    <div class="game-tournament-container">
      <div class="game-tournament-header">
        <LabelAchievements />
        <LabelValue coins :value="800" />
      </div>
      <div class="game-tournament-text">
        Bloomy Spring With Netent
      </div>
      <CustomButton class="participate">
        Participate
      </CustomButton>
    </div>
  </div>
</template>

<script>
  import CustomButton from "../common/CustomButton";
  import LabelAchievements from "../common/LabelAchievements";
  import LabelValue from "../common/LabelValue";
  export default {
    name: "GameTournament",
    components: {LabelValue, LabelAchievements, CustomButton}
  }
</script>

<style scoped lang="scss">
  .game-tournament {
    padding: 24px 0 28px;
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    background-image: url("../../../public/images/bloomy-spring-image.png");
    background-size: 100% 100%;
  }

  .game-tournament-container {
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .game-tournament-header {
    display: flex;
    justify-content: space-between;
  }

  .game-tournament-text {
    font-style: normal;
    font-weight: bold;
    font-size: 48px;
    text-align: left;
    color: #FFFFFF;
    text-shadow: 0 0 20px rgba(20, 19, 11, 0.75);
    padding: 0 24px;
    margin: auto;
    @media screen and (max-width: 1440px) {
      font-size: 36px;
    }
    @media screen and (max-width: 768px) {
      font-size: 28px;
    }
  }

  .participate {
    padding: 12px 60px;
  }
</style>
