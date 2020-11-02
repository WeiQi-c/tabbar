<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive" ><slot name="item-icon"></slot></div>
    <!-- <slot v-if="!isActive" name="item-icon"></slot> -->
    <div v-else><slot name="item-icon-active"></slot></div>
    <!-- <slot v-else name="item-icon-active"></slot> -->
    <div :style="activeStyle"><slot name="item-text"></slot></div>
    
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    props: {
      path: String,  // 从App.vue传进来 指定传进来的是字符串类型
      activeColor: {
        type: String,
        default: "#e95e9e"
      }
    },
    data() {
      return {
        // isActive: true
      }
    },
    computed: {
      isActive() {
        // 路径下是否包含当前页面地址 （等于-1 为不包含）
        return this.$route.path.indexOf(this.path) !== -1
      },
      activeStyle() {  // 处于活跃获取传进来的颜色
        return this.isActive ? {color: this.activeColor} : {}
      }
    },
    methods: {
      itemClick() {
        // 无跳转
        // this.$router.replace(this.path)
        // 有跳转
        this.$router.push(this.path)
      }
    },
  }

</script>

<style scoped>
  .tab-bar-item {
    flex: 1;
    text-align: center;
    height: 49px;
  }
  .tab-bar-item img {
    width: 24px;
    height: 24px;
  }

  /* .active {
    color: #e95e9e;
  } */
</style>
