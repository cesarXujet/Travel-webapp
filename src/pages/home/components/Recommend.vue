<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl"/>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1807/20/20e8b976e7ee4a92a3.img.jpg_200x200_4b90b05f.jpg',
        title: '东方山水乐园',
        desc: '暑期清凉游玩圣地，带上全家一起去'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/38/384b942cb06598ca3.img.jpg_200x200_a07af985.jpg',
        title: '乔波冰雪世界',
        desc: '暑期清凉游玩圣地，带上全家一起去'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/56/56dd8f7a275c4921a3.img.jpg_200x200_ec92fa6b.jpg ',
        title: '兜率天宫',
        desc: '暑期清凉游玩圣地，带上全家一起去'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/33/3312e54d3336baeca3.img.jpg_200x200_ca260c2c.jpg',
        title: '五泄丛林探险漂流',
        desc: '暑期清凉游玩圣地，带上全家一起去'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/06/ddb6a787c7b966df93835fbb.png_200x200_b91ad362.png',
        title: '绍兴古城',
        desc: '暑期清凉游玩圣地，带上全家一起去'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
