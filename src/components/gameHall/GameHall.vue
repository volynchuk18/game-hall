<template>
  <div class="game-hall-container">
    <GameHallBackground />
    <br>
    <UserBalance />
    <br>
    <br>
    <CatBar class="cat-bar" />
    <GameHallSearchBar />
    <div class="game-hall">
      <GameItem
        v-for="(_, index) in 44"
        :key="index"
      />
      <GameTournament
        class="game-item-big"
      />
      <GameAchievements
        class="game-item-medium"
      />
    </div>
  </div>
</template>

<script>
  import GameItem from "../common/GameItem";
  import GameTournament from "./GameTournament";
  import GameAchievements from "./GameAchievements";
  import GameHallBackground from "./GameHallBackground";
  import CatBar from "./CatBar";
  import GameHallSearchBar from "./GameHallSearchBar";
  import UserBalance from "../common/UserBalance";
  export default {
    name: "GameHall",
    components: {UserBalance, GameHallSearchBar, CatBar, GameHallBackground, GameAchievements, GameTournament, GameItem}
  }
</script>

<style scoped lang="scss">
  .game-hall {
    margin: 32px auto 0;
    padding: 0 100px;
    display: grid;
    grid-auto-rows: 1fr;
    grid-template-columns: repeat(6, 1fr);
    grid-gap: 20px;
  }

  .game-item-medium {
    grid-column-start: 5;
    grid-column-end: 7;
    grid-row-start: 1;
    grid-row-end: 3;
  }

  .game-item-big {
    grid-column-start: 1;
    grid-column-end: 3;
    grid-row-start: 3;
    grid-row-end: 6;
  }

  @media screen and (max-width: 1280px) {
    .game-hall {
      padding: 0 50px;
    }
  }

  @media screen and (max-width: 1024px) {
    .game-item-big {
      grid-column-start: 1;
      grid-column-end: 3;
      grid-row-start: 4;
      grid-row-end: 7;
    }

    .game-item-medium {
      grid-column-start: 5;
      grid-column-end: 7;
      grid-row-start: 1;
      grid-row-end: 4;
    }

    .game-hall {
      padding: 0 40px;
    }
  }
  @media screen and (max-width: 768px) {
    .game-hall {
      grid-gap: 16px;
    }
    .game-hall {
      grid-template-columns: repeat(4, 1fr);
    }

    .game-item-medium {
      grid-column-start: 1;
      grid-column-end: 3;
      grid-row-start: 4;
      grid-row-end: 7;
    }

    .game-item-big {
      grid-column-start: 3;
      grid-column-end: 5;
      grid-row-start: 4;
      grid-row-end: 7;
    }
  }
  @media screen and (max-width: 540px) {
    .game-hall {
      grid-gap: 8px;
      padding: 0 16px;
    }
  }
  @media screen and (max-width: 480px) {
    .game-hall {
      grid-template-columns: repeat(2, 1fr);
    }

    .game-item-medium {
      grid-column-start: 1;
      grid-column-end: 3;
      grid-row-start: 7;
      grid-row-end: 10;
    }

    .game-item-big {
      grid-column-start: 1;
      grid-column-end: 3;
      grid-row-start: 10;
      grid-row-end: 13;
    }
  }

</style>
