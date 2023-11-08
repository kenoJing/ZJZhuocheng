<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="logo"></div>
    <div class="wrapper">
      <el-menu mode="horizontal">
        <el-menu-item index="1">
          <RouterLink to="/">首页</RouterLink>
        </el-menu-item>
        <el-menu-item index="2">
          <RouterLink to="/about">公司简介</RouterLink>
        </el-menu-item>
        <el-menu-item index="3">
          <RouterLink to="/mechanical">机械设备</RouterLink>
        </el-menu-item>
        <el-menu-item index="4">
          <RouterLink to="/production">产品服务</RouterLink>
        </el-menu-item>
        <el-menu-item index="5">
          <RouterLink to="/solution">解决方案</RouterLink>
        </el-menu-item>
        <el-menu-item index="6">
          <RouterLink to="/contact">联系我们</RouterLink>
        </el-menu-item>
      </el-menu>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header .wrapper a {
  color: inherit;
  text-decoration: none;
}

header .wrapper a:hover {
  color: inherit;
  text-decoration: none;
}

header .wrapper a:visited {
  color: inherit;
  text-decoration: none;
}

header .wrapper a:active {
  color: inherit;
  text-decoration: none;
}

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
</style>
