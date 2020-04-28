<template>
  <div id="app">
    <GameHall />
  </div>
</template>

<script>
import GameHall from "./components/gameHall/GameHall";

export default {
  name: 'App',
  components: {
    GameHall,
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Proxima Nova Lt', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  margin: 0 auto;
}

body {
  margin: 0;
  display: inline-flex;
  width: 100%;
  background: #110F36;
}

*, ::after, ::before {
  box-sizing: border-box;
}
</style>
