<template>
  <div class="value">
    {{ value }}
    <img
      class="icon"
      src="/icons/icon-crystal.png"
      v-if="crystal"
    />
    <img
      class="icon"
      src="/icons/icon-coins.png"
      v-else-if="coins"
    />
  </div>
</template>

<script>
  export default {
    name: "LabelValue",
    props: {
      crystal: {
        type: Boolean,
        default: false
      },
      coins: {
        type: Boolean,
        default: false
      },
      value: {
        type: Number
      }
    }
  }
</script>

<style scoped>
  .value {
    top: 24px;
    padding-right: 20px;
    display: flex;
    align-items: center;
    font-weight: bold;
    font-size: 38px;
    line-height: 36px;
    color: white;
    border-radius: 0 24px 24px 0;
  }

  .icon {
    margin-left: 6px;
  }
</style>
