<script setup lang="ts">
import { RouterView } from "vue-router";
import { ref } from 'vue';

const curPath = ref( window.location.pathname);
</script>

<template>
  <header>
    <div class="logo"></div>
    <div class="wrapper">
      <el-menu mode="horizontal" ellipsis="false" router="true" :default-active="curPath">
        <el-menu-item index="/">
          首页
        </el-menu-item>
        <el-menu-item index="/about">
          公司简介
        </el-menu-item>
        <el-menu-item index="/mechanical">
          机械设备
        </el-menu-item>
        <el-menu-item index="/production">
          产品服务
        </el-menu-item>
        <el-menu-item index="/solution">
          解决方案
        </el-menu-item>
        <el-menu-item index="/contact">
          联系我们
        </el-menu-item>
      </el-menu>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  height: 127px;
  align-items: center;
}
header .logo {
  height: 100%;
  width: 700px;
}
header .wrapper {
  width: calc(100% - 700px);
}
header .wrapper .el-menu--horizontal {
  border-bottom: none;
  height: 80px;
}
header .wrapper .el-menu-item {
  font-size: 16px;
  font-weight: 700;
}
</style>
