<template>
  <div class="bonus-small">
    +{{ bonus }}
    <img
      class="icon"
      src="/icons/icon-coins.png"
    />
  </div>
</template>

<script>
  export default {
    name: "BonusSmall",
    props: ['bonus']
  }
</script>

<style scoped>
  .bonus-small {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 2px;
    font-family: 'Proxima Nova Th', sans-serif;
    font-weight: 800;
    font-size: 18px;
    color: #FFFFFF;
    background: #007AFF;
    border-radius: 12px;
  }

  .icon {
    margin-left: 2px;
    width: 26px;
    height: 20px;
  }
</style>
