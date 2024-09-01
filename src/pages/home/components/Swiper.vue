<template>
  <div class="sw-wrapper">
    <swiper ref="mySwiper" :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        // scrollbar:'.swiper-scrollbar',
        // autoplay: 5000,
        loop: true,
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM1b12000f4gegmj8C94_Q10.webp'
        },
        {
          id: '002',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM4c12000f9mrn7kB08A.webp'
        },
        {
          id: '003',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM5712000fa95gar8198.webp'
        },
        {
          id: '004',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM1b12000f4gegmj8C94_Q10.webp'
        },
        {
          id: '005',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM4c12000f9mrn7kB08A.webp'
        },
        {
          id: '006',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0AM5712000fa95gar8198.webp'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.sw-wrapper >>> .swiper-pagination-bullet-active {
  background-color: #fff;
}

.sw-wrapper {
  overflow: hidden;
  width: 100%;
  // height: 2.1067rem;
  // height: 0;
  // padding-bottom: 26.67%;
  background-color: #eee;
}

.sw-wrapper .swiper-img {
  width: 100%;
  // height: 100%;
}
</style>