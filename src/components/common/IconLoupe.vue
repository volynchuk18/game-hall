<template>
  <div @click="$emit('click')" class="icon-loupe">
    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M8.21474 0C3.67878 0 0 3.67796 0 8.21291C0 12.7479 3.67878 16.4258 8.21474 16.4258C12.7507 16.4258 16.4295 12.7479 16.4295 8.21291C16.425 3.67796 12.7507 0.00446354 8.21474 0ZM8.21474 13.5692C5.25476 13.5692 2.8573 11.1722 2.8573 8.21291C2.8573 5.25358 5.25476 2.85666 8.21474 2.85666C11.1747 2.85666 13.5722 5.25358 13.5722 8.21291C13.5677 11.1678 11.1703 13.5647 8.21474 13.5692Z" fill="white"/>
      <path d="M19.5814 17.5596L16.7241 14.7029C16.1661 14.145 15.2598 14.145 14.7017 14.7029C14.1436 15.2608 14.1436 16.1669 14.7017 16.7249L17.559 19.5815C18.1171 20.1395 19.0234 20.1395 19.5814 19.5815C20.1395 19.0236 20.1395 18.1175 19.5814 17.5596Z" fill="white"/>
    </svg>
  </div>
</template>

<script>
  export default {
    name: "IconLoupe"
  }
</script>

<style scoped lang="scss">
  .icon-loupe {
    width: 40px;
    height: 40px;
    border: 2px solid #007AFF;
    border-radius: 50%;
    box-shadow: 0 0 5px #007AFF;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      background: #007AFF;
    }
    &:active {
      box-shadow: none;
    }
  }
</style>
