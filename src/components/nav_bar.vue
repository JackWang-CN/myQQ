<!--首页顶部导航条-->
<template>
  <div id="nav_bar">
      <!-- 导航条 -->
      <div class="container nav_bar">
        <!-- 左导航 -->
        <div class="nav_left">
          <div class="logo">
            <img :src="imgLogo" alt="">
          </div>
          <div class="nav">
            <router-link to=''>首页</router-link>
            <router-link to=''>下载</router-link>
            <router-link to=''>动态</router-link>
          </div>
        </div>
        <!-- 右导航 -->
        <div class="nav_right">
          <router-link class='btns' to=''>注册</router-link>
          <router-link to=''>QQ会员</router-link>
          <router-link to=''>QQ安全</router-link>
          <router-link to=''>登录</router-link>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data(){
    return {
      imgLogo:require('../assets/images/logo.png')
    }
  },


}
</script>

<style lang='less'>
#nav_bar{
  .nav_bar{
    display: flex;
    justify-content: space-between;
    // 左导航
    .nav_left{
      display: flex;
      .logo{
        padding: 20px;
      }
      .nav{
        line-height: 86px;
        a{
          display: inline-block;
          padding: 0 20px;
          margin: 0 10px;
          height: 100%;
          &:hover{
          background: #12b7f5;
        }
        }
      }
    }
    // 右导航
    .nav_right{
      margin-top: 25px;
        a{
            margin:0 20px;
            &.btns{
            display: inline-block;
            padding: 13px 32px;
            background: #24C1FC;
            color: #fff;
            border-radius: 25px;
            margin-right: 20px;
            font-size: 18px;
        }
      }
    }
  }
  
}


</style>