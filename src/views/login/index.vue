<template>
   <div class='login'>
      <el-card class="login-card">
        <div class="logo">
            <img src="../../assets/img/logo_index.png" alt="">
        </div>
        <!-- 表单组件 el-form表单容器 -->
        <el-form style="margin-top:20px">
            <!-- 表单项 -->
            <el-form-item>
            <!-- 放置组件内容 -->
              <el-input placeholder="请输入手机号"></el-input>
            </el-form-item>
            <el-form-item>
              <el-input style="width:260px" placeholder="验证码"></el-input>
               <el-button style="float:right">发送验证码</el-button>
            </el-form-item>
            <el-form-item>
                <el-checkbox>我已阅读并同意用户协议和隐私条款</el-checkbox>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" style="width:100%">登录</el-button>
            </el-form-item>
        </el-form>
      </el-card>
   </div>
</template>

<script>
export default {

}
</script>

<style lang='less' scoped>
// lang属性 是对css进行语言指定
// scoped 只针对当前组件起作用
// 100vh 占据当前可视窗口的100%
.login{
    background: url(../../assets/img/login_bg.jpg);
    background-size: cover;
    height:100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    .login-card{
        width: 420px;
        height: 340px;
        .logo{
           text-align: center;
           img{
               height: 35px;
           }
        }
    }
}
</style>