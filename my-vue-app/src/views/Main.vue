<template>
  <div class="common-layout">
    <el-container>
      <el-aside width="200px">
        <CommonAside />
      </el-aside>
      <el-container class="r-container">
        <el-header>
          <CommonHeader />
        </el-header>
        <el-main>
          <router-view />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script setup>
import CommonHeader from "../components/CommonHeader.vue";
import CommonAside from "../components/CommonAside.vue";
</script>

<style lang="less" scoped>
.r-container {
  flex-wrap: nowrap;
}
</style>
