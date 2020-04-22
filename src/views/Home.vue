<template>
  <div id="home">
    <div class="wrap">
      <div class="top_nav"><mynav/></div>
        <el-carousel :autoplay='false' :interval="5000" arrow="never" height='965px'>
          <el-carousel-item v-for="item in 2" :key="item" label='〇'>
          </el-carousel-item>
        </el-carousel>
      </div>
  </div>
</template>

<script>
import mynav from '../components/nav_bar'
export default {
  name: 'Home',
  components:{
    mynav
  }


}
</script>

<style lang='less'>  
  .el-carousel__item:nth-child(2n) {
    background: url('../assets/images/bg_img2.jpeg') 50% 50% no-repeat;
    background-size: cover;
    background-position: 50% 50%;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background: url('../assets/images/pc_bg.jpg') no-repeat;
    background-size: cover;
    background-position: 50% 50%;
  }
  .el-carousel__button{
    span{
      
    }
  }

  .wrap{
    position: relative;
  }
  .top_nav{
    position: absolute;
    width: 100%;
    z-index: 999;
  }


</style>