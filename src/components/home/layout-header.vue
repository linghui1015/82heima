<template>
  <el-row type='flex' justify='space-between'>
      <el-col :span="6">
        <el-col>
          <i class="el-icon-s-unfold"></i>
          <span>江苏传智播客教育科技股份有限公司</span>
        </el-col>
      </el-col>
      <el-col :span="2">
        <img class="head-img" src="../../assets/img/avatar.jpg" alt="">
         <el-dropdown trigger="click">
            <span class="el-dropdown-link">
        下拉菜单<i class="el-icon-arrow-down el-icon--right"></i>
      </span>
      <el-dropdown-menu slot="dropdown">
        <el-dropdown-item icon="el-icon-plus">黄金糕</el-dropdown-item>
        <el-dropdown-item icon="el-icon-circle-plus">狮子头</el-dropdown-item>
        <el-dropdown-item icon="el-icon-circle-plus-outline">螺蛳粉</el-dropdown-item>
        <el-dropdown-item icon="el-icon-check">双皮奶</el-dropdown-item>
        <el-dropdown-item icon="el-icon-circle-check">蚵仔煎</el-dropdown-item>
      </el-dropdown-menu>
         </el-dropdown>
      </el-col>
  </el-row>
</template>

<script>
export default {
    
}
</script>

<style>

</style>