<template>
  <div class="wrapper">
    <div class="list" ref="listWrapper">
      <div class="hot-cities">
        <div class="hot-cts-title">热门城市</div>
        <ul class="clearfix">
          <!-- assets/styles/border.css中设置了 border-top 和 border-topleft -->
          <li>阿拉尔</li>
          <li class="border-left">北京</li>
          <li class="border-left">成都</li>
          <li class="border-top">阿拉尔</li>
          <li class="border-left">北京</li>
          <li class="border-left">成都</li>
          <li class="border-top">阿拉尔</li>
          <li class="border-left">北京</li>
          <li class="border-left">成都</li>
          <li class="border-top">阿拉尔</li>
          <li class="border-left">北京</li>
          <li class="border-left">成都</li>
        </ul>
      </div>
      <div class="aplhabet-menu">
        <div class="aplhabet-menu-title">字母排序</div>
        <ul class="clearfix">
          <li>A</li>
          <li>B</li>
          <li>C</li>
          <li>D</li>
          <li>E</li>
          <li>F</li>
          <li>G</li>
          <li>H</li>
          <li>I</li>
          <li>J</li>
          <li>K</li>
          <li>L</li>
          <li>M</li>
          <li>N</li>
          <li>O</li>
          <li>P</li>
          <li>Q</li>
          <li>R</li>
          <li>S</li>
          <li>T</li>
          <li>U</li>
          <li>V</li>
          <li>W</li>
          <li>X</li>
          <li>Y</li>
          <li>Z</li>
        </ul>
      </div>
      <div class="aplhabet-list">
        <div class="aplhabet-list-title">A</div>
        <ul class="clearfix">
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
          <li>阿拉尔</li>
        </ul>
        <div class="aplhabet-list-title">A</div>
        <ul class="clearfix">
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
          <li>北京</li>
        </ul>
        <div class="aplhabet-list-title">A</div>
        <ul class="clearfix">
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
          <li>成都</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted: function() {
    this.scroll = new BScroll('.wrapper', {
      click: true
    })
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl';
@import '~styles/mixins.styl';

div {
  box-sizing: border-box;
}

li {
  list-style: none
}

.clearfix::after {
  display: block;
  content: "";
  clear: both;
}

.list {
  position: absolute;
  top: .88rem;
  bottom: 0;
  left: 0;
  right: 0;
  // overflow: hidden;
}

.hot-cities {
  width: 100%;
  height: 4.32rem;
}

.hot-cities .hot-cts-title,
.aplhabet-menu .aplhabet-menu-title,
.aplhabet-list .aplhabet-list-title {
  width: 100%;
  height: 0.72rem;
  line-height: .72rem;
  padding: 0 .2rem;
  font-size: .26rem;
  background-color: #f5f5f5;
  color: $darkTxtColor;
}

.hot-cities ul li {
  float: left;
  width: 33%;
  height: .9rem;
  line-height: .9rem;
  text-align: center;
  color: $darkTxtColor;
}

.aplhabet-menu ul {
  height: 4.2rem;
  margin: .3rem 0;
}

.aplhabet-menu ul li {
  float: left;
  width: 16.66%;
  height: .9rem;
  line-height: .9rem;
  text-align: center;
}

.aplhabet-list ul li {
  float: left;
  width: 25%;
  height: .9rem;
  line-height: .9rem;
  text-align: center;
  text-indent: .1rem;
  ellipsis();
}
</style>