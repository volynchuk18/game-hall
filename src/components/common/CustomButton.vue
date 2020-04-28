<template>
  <button
    class="custom-button"
    @click="$emit('click')"
  >
    <slot />
  </button>
</template>

<script>
  export default {
    name: "CustomButton"
  }
</script>

<style scoped lang="scss">
  .custom-button {
    border: none;
    cursor: pointer;
    background: #FFFFFF;
    border-radius: 24px;
    padding: 12px 40px;
    margin: 0 auto;
    font-size: 16px;
    font-family: 'Proxima Nova Rg', sans-serif;
    font-weight: bold;
    color: #5600CB;
    transition: 0.3s;
    outline: none;
    width: fit-content;
    &:hover {
      box-shadow: 0 0 12px #FFFFFF;
    }
    &:active {
      color: white;
      background: #5600CB;
    }
  }
</style>
