<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item path="/home" :activeColor="activeColor">
        <img
          slot="item-icon"
          src="./assets/img/tabbar/home-outline.svg"
          alt=""
        >
        <img
          slot="item-icon-active"
          src="./assets/img/tabbar/home-active.svg"
          alt=""
        >
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/cart" :activeColor="activeColor">
        <img
          slot="item-icon"
          src="./assets/img/tabbar/cart-outline.svg"
          alt=""
        >
        <img
          slot="item-icon-active"
          src="./assets/img/tabbar/cart-active.svg"
          alt=""
        >
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/category" :activeColor="activeColor">
        <img
          slot="item-icon"
          src="./assets/img/tabbar/grid-outline.svg"
          alt=""
        >
        <img
          slot="item-icon-active"
          src="./assets/img/tabbar/grid-active.svg"
          alt=""
        >
        <div slot="item-text">更多</div>
      </tab-bar-item>
      <tab-bar-item path="/profile" :activeColor="activeColor">
        <img
          slot="item-icon"
          src="./assets/img/tabbar/person-outline.svg"
          alt=""
        >
        <img
          slot="item-icon-active"
          src="./assets/img/tabbar/person-active.svg"
          alt=""
        >
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>

<script>
import TabBar from './components/tabbar/tabBar.vue'
import TabBarItem from './components/tabbar/tabBarItem.vue'
export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem
  },
  data() {
    return {
      activeColor: 'black'
    }
  }
}
</script>

<style>
</style>
