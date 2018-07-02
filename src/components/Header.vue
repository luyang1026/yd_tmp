<template>
  <div class="container">
    <div class="logo"></div>
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
      <el-submenu index="1">
        <template slot="title">商户管理</template>
        <el-menu-item index="1-1">商户管理</el-menu-item>
        <el-menu-item index="1-2">商户归属管理</el-menu-item>
      </el-submenu>
      <el-submenu index="2">
        <template slot="title">商品SKU管理</template>
        <el-menu-item index="2-1">商品SKU管理</el-menu-item>
        <el-menu-item index="2-2">商品SPU管理</el-menu-item>
        <el-menu-item index="2-3">品牌管理</el-menu-item>
        <el-menu-item index="2-4">特价商品</el-menu-item>
      </el-submenu>
      <el-submenu index="3">
        <template slot="title">需求单管理</template>
        <el-menu-item index="3-1">需求单管理</el-menu-item>
        <el-menu-item index="3-2">需求单归属分配</el-menu-item>
      </el-submenu>
      <el-submenu index="4">
        <template slot="title">运营管理</template>
        <el-menu-item index="4-1">新增商品审核</el-menu-item>
        <el-menu-item index="4-2">优惠券</el-menu-item>
        <el-menu-item index="4-3">消息推送</el-menu-item>
        <el-menu-item index="4-4">大宗批发</el-menu-item>
      </el-submenu>
      <el-submenu index="5">
        <template slot="title">员工管理</template>
        <el-menu-item index="5-1">新建员工</el-menu-item>
        <el-menu-item index="5-2">员工管理</el-menu-item>
        <el-menu-item index="5-3">部门管理</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: '1-1'
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>
<style lang="stylus" scoped>
.container
  display flex
  border-bottom solid 1px #e6e6e6
  justify-content space-between
  .logo
    width 40%
  .el-menu-demo
    border none
</style>
<style lang="stylus">
  &.el-menu--horizontal>.el-submenu
    .el-submenu__title
      line-height 55px
      height 55px
</style>

