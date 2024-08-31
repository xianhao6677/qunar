<template>
  <div class="sw-wrapper">
    <swiper ref="mySwiper" :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- <swiper-slide>
        <img class="swiper-img" src="https://imgs.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg" />
      </swiper-slide> -->
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
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg'
        },
        {
          id: '002',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg'
        },
        {
          id: '003',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg'
        },
        {
          id: '004',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg'
        },
        {
          id: '005',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1606/88/56f7f4bd0493fe.jpg_r_640x214_f8c0994a.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.sw-wrapper >>> .swiper-pagination-bullet-active {
  margin-bottom: 1rem;
  background-color: #fff;
}

.sw-wrapper {
  // overflow: hidden;
  width: 100%;
  height: 2.1067rem;
  // padding-bottom: 26.67%;
  background-color: #eee;
}

.sw-wrapper .swiper-img {
  width: 100%;
  height: 100%;
}
</style>