<template>
   <!-- 最外层容器 -->
   <el-container>
       <!-- 左侧导航 -->
       <el-aside style='width:200px;background-color:#323745;overflow: hidden;'>
           <layout-aside></layout-aside>
       </el-aside>
       <!-- 右侧 -->
       <el-conteiner id="rightBox">
           <!-- 头部 -->
           <el-header>
              <layout-header></layout-header>
           </el-header>
           <!-- 主要区域 -->
           <el-main>主体</el-main>
       </el-conteiner>
   </el-container>
</template>

<script>
import layoutAside from '../../components/home/layout-aside'
import layoutHeader from '../../components/home/layout-header'
export default {
  components :{
   'layout-aside' : layoutAside ,
   'layout-header' : layoutHeader
   }
}
</script>

<style>
#rightBox{
    width: 100%;
}
</style>