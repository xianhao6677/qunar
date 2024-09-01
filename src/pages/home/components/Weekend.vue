<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <router-link to="/detail" tag="li" class="list-item" v-for="item in recommendList" :key="item.id">
        <div class="item-img">
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <div class="info-title">{{item.title}}</div>
          <div class="info-comment">{{ item.comment }}</div>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data: function() {
    return {
      recommendList: [
        {
          id: '001',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
          title: '清远周边逛',
          comment: '人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？'
        },
        {
          id: '002',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/b8/5d599bbdcf8b57.jpg_r_640x214_2ee055e3.jpg',
          title: '浮在海上的绿洲',
          comment: '南国滨海之城，避寒胜地，有暖暖的阳光，海风习习，吃着海鲜逛逛老街多惬意啊'
        },
        {
          id: '003',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg',
          title: '广州必打卡',
          comment: '感受现代与传统相融合的广州'
        },
        {
          id: '004',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
          title: '阳江温泉知多少',
          comment: '这里的天空和大海让人心旷神怡，配上舒缓的优美音乐，泡个暖暖的温泉岂不美哉'
        },
        {
          id: '005',
          imgUrl: 'https://imgs.qunarzz.com/sight/source/1606/88/56f7f4bd0493fe.jpg_r_640x214_f8c0994a.jpg',
          title: '签到广州长隆',
          comment: '带上宝贝，来这里感受不同的亲子游主题活动。拉近你和孩子的距离，亲子同乐，寓教于乐！'
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
  font-size: .28rem;
  background-color: #eee;
}

.list-item {
  // display: flex;
  // position: relative;
  width: 100%;
  // height: 2.4rem;
  margin-bottom: .1rem
  background-color: skyblue;
}

.list-item .item-img {
  width: 100%;
	height: 0;
	padding-bottom: 37.1%;
  border-radius: .1rem;
  overflow: hidden;
}

.list-item .item-img img {
  width: 100%;
  // height: 100%;
}

.list-item .item-info {
  padding: .14rem .2rem .2rem;
  min-width: 0;
}

.item-info .info-title {
  width: 100%;
  height: 0.48rem;
  line-height: .48rem;
  font-size: .28rem;
  font-weight: 700;
  ellipsis();
}

.item-info .info-comment {
  width: 100%;
  height: 0.42rem;
  line-height: .42rem;
  font-size: .24rem;
  color: $lightTxtColor;
  ellipsis();
}
</style>