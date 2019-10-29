<template>
  <view class="content">
    <navigator url="/pages/issue/house/house" hover-class="none" class="uni-flex-item issueBox bgOne">
      <view class="issueImg">
        <image src="/static/images/2019cfsj_98.png" mode=""></image>
      </view>
      <view class="issueTitle">发布找房</view>
      <view class="issueWord">万千商铺任你挑选</view>
    </navigator>
    <navigator url="/pages/issue/plant/plant" hover-class="none" class="uni-flex-item issueBox bgTwo">
      <view class="issueImg">
        <image src="/static/images/2019cfsj_99.png" mode=""></image>
      </view>
      <view class="issueTitle">发布转厂房</view>
      <view class="issueWord">平均30天转出商铺</view>
    </navigator>
    <navigator url="/pages/issue/office/office" hover-class="none" class="uni-flex-item issueBox bgThree">
      <view class="issueImg">
        <image src="/static/images/2019cfsj_100.png" mode=""></image>
      </view>
      <view class="issueTitle">发布转写字楼</view>
      <view class="issueWord">平均30天租出厂房</view>
    </navigator>
  </view> 
</template>

<script>
  export default{
    data(){
      return{
        
      }
    }
  }
  
</script>

<style lang="scss" scoped>
  .content{
    box-sizing:border-box;
    width:100%;
    height:100%;
    padding:30rpx 30rpx 0;
    display:flex;
    flex-direction:column;
  }
  
  .issueBox{
    margin-bottom:30rpx;
    background:#D9D9D9;
    border-radius:10rpx;
    overflow:hidden;
    position:relative;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    .issueImg{
      width:110rpx;
      height:110rpx;
      border-radius:50%;
      overflow:hidden;
    }
    .issueTitle{
      font-size:34rpx;
      font-weight:bold;
      color:#000000;
      padding:10rpx 0;
    }
    .issueWord{
      font-size:28rpx;
      font-weight:600;
      color:#666666;
    }
  }
  
  .bgOne{
    background-image:url(~@/static/images/2019cfsj_95.png);
    background-size:100% 100%;
    background-repeat: no-repeat;
  }
  
  .bgTwo{
    background-image:url(~@/static/images/2019cfsj_96.png);
    background-size:100% 100%;
    background-repeat: no-repeat;
  }
  
  .bgThree{
     background-image:url(~@/static/images/2019cfsj_97.png);
     background-size:100% 100%;
     background-repeat: no-repeat;
  }
  
</style>
