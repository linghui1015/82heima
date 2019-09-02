<template>
   <div class='login'>
      <el-card class="login-card">
        <div class="logo">
            <img src="../../assets/img/logo_index.png" alt="">
        </div>
        <!-- 表单组件 el-form表单容器 -->
        <el-form :model="loginForm" :rules="loginRules" style="margin-top:20px">
            <!-- 表单项 -->
            <el-form-item prop="mobile">
            <!-- 放置组件内容 -->
              <el-input v-model="loginForm.mobile" placeholder="请输入手机号"></el-input>
            </el-form-item>
            <el-form-item prop="code">
              <el-input v-model="loginForm.code" style="width:260px" placeholder="验证码"></el-input>
               <el-button style="float:right">发送验证码</el-button>
            </el-form-item>
            <el-form-item prop="check">
                <el-checkbox v-model="loginForm.check">我已阅读并同意用户协议和隐私条款</el-checkbox>
            </el-form-item>
            <el-form-item>
                <el-button @click="login" type="primary" style="width:100%">登录</el-button>
            </el-form-item>
        </el-form>
      </el-card>
   </div>
</template>

<script>
export default {
    data () {
    let validator = function (rule, value, callBack) {
        if (value) {
            callBack()
        } else {
            callBack(new Error('请您必须勾选同意选择'))
        }
    }
        return {
            loginForm: {
                mobile: '', // 手机号
                code: '', //验证码
                check: false // 是否勾选
            },
            //定义rules 校验规则 表单根据规则校验 没有规则 就没有校验
            // key(字段名): value(数组对象=> 多个 => 一个字段 可以有一个或多个校验规则)
            loginRules:{
               mobile:[{
                   required:true,//必填项
                   message: '手机号不能为空' //为满足就会提示
               },{
                 pattern:/^1[3456789]\d{9}$/,//正则表达式
                 message:'手机号格式不正确,请从新输入'
               }],
               code:[{
                   required:true,
                   message: '验证码不能为空'
               },{
                 pattern:/^\d{6}$/,
                 message:'验证码必须为6位数字'
               }],
               check:[{
                   validator
               }]
            }
        }
    },
    methods: {
        login () {
            this.$message('提示消息')
        }
    }
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