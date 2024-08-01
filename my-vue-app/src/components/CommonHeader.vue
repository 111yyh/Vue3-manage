<template>
  <div class="header">
    <div class="l-content">
      <!-- 图标展示 -->
      <el-button size="small">
        <el-icon :size="14">
          <Menu />
        </el-icon>
      </el-button>
    </div>
    <div class="r-content">
      <el-dropdown>
        <span class="el-dropdown-link">
          <img class="user" :src="getImageSrc('image')" alt="" />
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>个人中心</el-dropdown-item>
            <el-dropdown-item>退出</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
  </div>
</template>

<script setup>
const getImageSrc = (image) => {
  return new URL(`../assets/${image}.png`, import.meta.url).href;
};
</script>

<style lang="less" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
.r-content {
  .user {
    width: 40px;
    height: 40px;
    border-radius: 50%;
  }
}
</style>
