<template>
  <div class="icons-wrapper">
    <swiper :options="swiperOptions">
      <!-- slides -->
      <swiper-slide v-for="(page, idx) in pages" :key="idx">
        <div class="icon-box" v-for="item in page" :key="item.id">
          <div class="icon-img-box">
            <img class="icon-img" :src="item.imgUrl" alt="">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data: function() {
    return {
      swiperOptions: {
        autoplay: false
      },
      iconsList: [
        {
          id: '001',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '002',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '003',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '004',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '005',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '006',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '007',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '008',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        },
        {
          id: '009',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          desc: '景点门票'
        }
      ]
    }
  },
  computed: {
    pages: function() {
      var pages = []
      this.iconsList.forEach(function(item, idx) {
        var page = Math.floor(idx / 8)
        if(!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })

      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl';
@import '~styles/mixins.styl';
.icons-wrapper {
  width: 100%;
  height: 0;
  margin-top: .1rem;
  padding-bottom: 50%;
}

.icons-wrapper .icon-box {
  position: relative;
  float: left;
  width: 25%;
  height: 0;
  padding-bottom: 25%;;
}

.icons-wrapper .icon-box .icon-img-box {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: .44rem;
}

.icons-wrapper .icon-box .icon-img-box .icon-img {
  display: block;
  height: 100%;
  margin: 0 auto;
}

.icons-wrapper .icon-box .icon-desc {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: .44rem;
  line-height: .44rem;
  text-align: center;
  color: $darkTxtColor;
  ellipsis();
}
</style>