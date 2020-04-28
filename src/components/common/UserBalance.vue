<template>
  <div class="user-balance">
    <span class="user-balance-value">
      {{ title }}
    </span>
  </div>
</template>

<script>
  export default {
    name: "UserBalance",
    data() {
      return {
        balance: {
          value: 2253674.555,
          currency: 'euro'
        }
      }
    },
    computed: {
      title() {
        return `${this.currencyIcon}${this.formattedValue}`
      },
      currencyIcon() {
        switch (this.balance.currency) {
          case "euro":
            return '€';
          case "dollar":
            return '$'
        }
        return ''
      },
      formattedValue() {
        const formatNumber = num => {
          return num.toString().replace(/(\d)(?=(\d{3})+(?!\d))/g, '$1 ')
        }
        return formatNumber(this.balance.value.toFixed(2))
      }
    }
  }
</script>

<style scoped lang="scss">
  .user-balance {
    height: 44px;
    position: relative;
    border: 2px solid #61C200;
    box-sizing: border-box;
    box-shadow: 0 0 5px #61C200;
    border-radius: 24px 0 0 24px;
    padding: 10px 24px 10px 32px;
    font-weight: bold;
    font-size: 16px;
    color: #FFFFFF;
    display: inline-flex;
    cursor: pointer;
    &::after {
      content: "";
      position: absolute;
      width: 40px;
      height: calc(100% + 4px);
      top: -2px;
      left: calc(100% + 2px);
      border: 2px solid #61C200;
      box-shadow: 0 0 5px #61C200;
      border-radius: 0 24px 24px 0;
      background: #61C200 url("../../../public/icons/icon-deposit.svg") no-repeat 40% 40%;
    }
    &:hover {
      box-shadow: 0 0 10px #61C200;
      &::after {
        box-shadow: 0 0 10px #61C200;
      }
    }
    &:active {
      box-shadow: 0 0 12px #61C200;
      &::after {
        box-shadow: 0 0 12px #61C200;
      }
    }
  }

  .user-balance-value {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    max-width: 110px;
  }
</style>
