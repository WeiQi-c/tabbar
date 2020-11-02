<template>
    <tab-bar>     <!-- 与 TabBarItem.vue 中的插槽solt 一一对应 -->
      <!-- <tab-bar-item path="/home" activeColor="red"> -->     <!-- activeColor 传入活跃状态时改变的颜色 -->
      <tab-bar-item path="/home">
        <img slot="item-icon" src="../assets/img/tabbar/首页.svg" alt="">
        <img slot="item-icon-active" src="../assets/img/tabbar/首页-active.svg" alt="">
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category">
        <img slot="item-icon" src="../assets/img/tabbar/类目 品类 分类 类别.svg" alt="">
        <img slot="item-icon-active" src="../assets/img/tabbar/类目 品类 分类 类别-active.svg" alt="">
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart">
        <img slot="item-icon" src="../assets/img/tabbar/购物车.svg" alt="">
        <img slot="item-icon-active" src="../assets/img/tabbar/购物车-active.svg" alt="">
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile">
        <img slot="item-icon" src="../assets/img/tabbar/我的.svg" alt="">
        <img slot="item-icon-active" src="../assets/img/tabbar/我的-active.svg" alt="">
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
</template>

<script>
  import TabBar from '../components/tabbar/TabBar'
  import TabBarItem from '../components/tabbar/TabBarItem'

  export default {
    name: "MainTabBar",
    components: {
      TabBar,
      TabBarItem
    }
  }

</script>

<style scoped>
  
</style>
