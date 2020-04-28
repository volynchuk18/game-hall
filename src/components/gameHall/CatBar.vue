<template>
  <div class="cat-bar">
    <swiper :options="swiperOptions">
        <swiper-slide
          class="cat-item"
          :key="index" v-for="(_, index) in items"
        >
          <img class="cat-item-img" :src="getImgUrl(index)">
          <div>
            {{ index }}
          </div>
        </swiper-slide>
    </swiper>
  </div>
</template>

<script>
  export default {
    name: "CatBar",
    data() {
      return {
        swiperOptions: {
          slidesPerView: 'auto',
          spaceBetween: 8,
          breakpoints: {
            768: {
              allowSlidePrev: false,
              allowSlideNext: false,
            },
            0: {
              allowSlidePrev: true,
              allowSlideNext: true,
            },
          }
        },
        items: {
          provider: {},
          recent: {},
          top: {},
          slots: {},
          live: {},
          jackpot: {},
          table: {},
          favorite: {},
        }
      }
    },
    methods: {
      getImgUrl(pic) {
        return require('../../../public/icons/catBar/' + pic + '.png')
      }
    }
  }
</script>

<style scoped lang="scss">
  .cat-bar {
    width: 867px;
    display: inline-flex;
    @media screen and (max-width: 768px) {
      width: 100vw
    }
  }

  .cat-item {
    width: 100px !important;
    @media screen and (max-width: 1024px) {
      width: 76px !important;
    }
    @media screen and (max-width: 769px) {
      &:first-child {
        margin-left: 16px;
      }
    }
    font-family: 'Proxima Nova Bl', sans-serif;
    text-transform: capitalize;
    color: white;
    font-weight: 900;
    font-size: 13px;
    cursor: pointer;
    transition: 0.3s;
    &:not(:last-child) {
      margin-right: 8px !important;
    }
    &:hover {
      color: #FFCD00;
      .cat-item-img {
        box-shadow: 0 10px 30px #0058E3;
      }
    }
  }

  .cat-item-img {
    transition: box-shadow 0.3s ease-in-out 0s;
    border-radius: 30%;
    @media screen and (max-width: 1024px) {
      width: 76px !important;
    }
  }

  .custom-slide-class {
    width: 100px !important;
  }
</style>
