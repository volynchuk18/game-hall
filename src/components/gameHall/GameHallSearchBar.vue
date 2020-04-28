<template>
  <form @submit.prevent="submit" class="search-bar-container">
    <input placeholder="Search..." class="search-bar">
    <IconLoupe @click="submit" class="icon-loupe" />
  </form>
</template>

<script>
  import IconLoupe from "../common/IconLoupe";
  export default {
    name: "GameHallSearchBar",
    components: {IconLoupe},
    methods: {
      submit() {
        console.log('submit')
      }
    }
  }
</script>

<style scoped lang="scss">
  .search-bar-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 16px;
  }

  .search-bar {
    width: 766px;
    height: 40px;
    padding-left: 20px;
    background: rgba(86, 0, 203, 0.5);
    border-radius: 60px;
    border: none;
    outline: none;
    font-weight: bold;
    font-size: 14px;
    color: #FFFFFF;
    &::placeholder {
      color: rgba(255, 255, 255, 0.4);
    }
    @media screen and (max-width: 768px) {
      width: 80vw
    }
  }

  .icon-loupe {
    margin-left: 12px;
  }
</style>
