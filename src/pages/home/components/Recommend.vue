<template>
  <div>
    <div class="recommend-title">
      <span class="iconfont icon-heart">&#xe640;</span>
      猜你喜欢
    </div>
    <ul>
      <router-link to="/detail" tag="li" class="list-item" v-for="item in recommendList" :key="item.id">
        <div class="item-img">
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="item-img-tag">{{item.tag}}</div>
        <div class="item-info">
          <div class="inner-box">
            <div class="info-title">{{item.title}}</div>
            <div class="info-comment">
              <span class="iconfont icon-star"></span>
              <span class="iconfont icon-star"></span>
              <span class="iconfont icon-star"></span>
              <span class="iconfont icon-star"></span>
              <span class="iconfont icon-star"></span>
              <span class="comment-num">{{item.commentNum}}条评论</span>
            </div>
            <div class="info-price">
              <span class="price">￥<em>{{item.price}}</em></span>起
              <span class="district">{{item.district}}</span>
            </div>
          </div>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data: function() {
    return {
      recommendList: [
        {
          id: '001',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/dc9bebac-9f1e-440e-a690-7355a19267e6.jpg_200x200_c8fb3689.jpg',
          tag: '随买随用',
          title: '广州塔',
          commentNum: '83023',
          price: '147.19',
          district: '海珠区'
        },
        {
          id: '002',
          imgUrl: 'https://imgs.qunarzz.com/piao_qsight_web_piao_qsight_web/31724145300246.jpg_200x200_687fd4f3.jpg',
          tag: '随买随用',
          title: '长隆野生动物世界',
          commentNum: '281789',
          price: '300',
          district: '广州长隆野生动物世界'
        },
        {
          id: '003',
          imgUrl: 'https://imgs.qunarzz.com/piao_qsight_web_piao_qsight_web/21724145238877.jpg_200x200_54f0a8c9.jpg',
          tag: '随买随用',
          title: '长隆水上乐园',
          commentNum: '88202',
          price: '99',
          district: '广州长隆水上乐园'
        },
        {
          id: '004',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/82a9b09d-577a-48f0-ae04-0137e2703ec9.jpg_200x200_8303d5e7.jpg',
          tag: '随买随用',
          title: '广州动物园',
          commentNum: '14547',
          price: '29.9',
          district: '越秀区'
        },
        {
          id: '005',
          imgUrl: 'https://qimgs.qunarzz.com/piao_qsight_provider_piao_qsight_web/8a2047f3-9e4e-4531-a616-b45586061242.png_200x200_e73d054c.png',
          tag: '随买随用',
          title: '广东科学中心',
          commentNum: '45553',
          price: '60',
          district: '番禺区'
        },
        {
          id: '006',
          imgUrl: 'https://imgs.qunarzz.com/piao_qsight_web_piao_qsight_web/5-21724145384087.jpg_200x200_a47658db.jpg',
          tag: '随买随用',
          title: '长隆欢乐世界',
          commentNum: '127631',
          price: '250',
          district: '广州长隆欢乐世界'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl';
@import '~styles/mixins.styl';
div {
  box-sizing: border-box;
}
.recommend-title {
  width: 100%;
  height: 0.8rem;
  line-height: .8rem;
  margin-top: .2rem;
  padding: 0 .2rem;
  font-size: .32rem;
  background-color: #eee;
}

.recommend-title .icon-heart {
  color: #FF4040;
}

.list-item {
  display: flex;
  position: relative;
  width: 100%;
  height: 2.4rem;
}

.list-item .item-img {
  width: 2.4rem;
	height: 2.4rem;
	padding: .2rem;
}

.list-item .item-img img {
  width: 100%;
}

.list-item .item-img-tag {
  position: absolute;
  top: .2rem;
  left: .2rem;
  width: 1.02rem;
	height: .38rem;
  line-height: .38rem;
	background-image: url(https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png);
  background-size: 100% 100%;
  font-size: .2rem;
  color: #fff;
  text-indent: .04rem;
}

.list-item .item-info {
  flex: 1;
  padding: .4rem .1rem;
  min-width: 0;
}

.list-item .item-info .inner-box {
  width: 100%;
  height: 100%;
}

.item-info .inner-box .info-title {
  width: 100%;
  height: 0.6rem;
  font-size: .32rem;
  font-weight: 700;
  ellipsis();
}

.item-info .inner-box .info-comment {
  width: 100%;
  height: 0.4rem;
  line-height: .4rem;
  font-size: .24rem;
}

.item-info .inner-box .info-comment .icon-star {
	font-size: .2rem;
	color: #ffb436;
}

.item-info .inner-box .info-comment .comment-num {
	color: $lightTxtColor;
}

.item-info .inner-box .info-price {
  position: relative;
	width: 100%;
	height: .6rem;
	line-height: .6rem;
	color: $lightTxtColor;
}

.item-info .inner-box .info-price span {
	font-size: .24rem;
}

.item-info .inner-box .info-price .price {
	color: #ff8300;
}

.item-info .inner-box .info-price .price em {
	font-size: .4rem;
}

.item-info .inner-box .info-price .district {
	position: absolute;
	bottom: 0;
	right: .24rem;
}
</style>