<template>
  <view class="">
    <view class="swiperBox">
      <swiper class="swiper" :indicator-dots="false" :autoplay="true" :interval="3000" :duration="1000">
        <swiper-item>
            <image src="/static/images/2019cfsj_1.png"></image>
        </swiper-item>
        <swiper-item>
           <image src="/static/images/2019cfsj_1.png"></image>
        </swiper-item>
        <swiper-item>
            <image src="/static/images/2019cfsj_1.png"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="category uni-inline-item">
      <view class="uni-flex-item cateItem">
        <view class="cateImg">
          <image src="/static/images/2019cfsj_42.png"></image>
        </view>
        <view class="">
          娱乐
        </view>
      </view>
      <view class="uni-flex-item cateItem">
        <view class="cateImg">
          <image src="/static/images/2019cfsj_42.png"></image>
        </view>
        <view class="">
          国际
        </view>
      </view>
      <view class="uni-flex-item cateItem">
        <view class="cateImg">
          <image src="/static/images/2019cfsj_42.png"></image>
        </view>
        <view class="">
          运动
        </view>
      </view>
      <view class="uni-flex-item cateItem">
        <view class="cateImg">
          <image src="/static/images/2019cfsj_42.png"></image>
        </view>
        <view class="">
          种类一
        </view>
      </view>
    </view>
    
    <view class="recommendBox">
      <view class="recmTitle">每日推荐</view>
      <navigator class="recmItem uni-inline-item" url="/pages/message/msgDetails/msgDetails" v-for="(item,index) in 6" :key="index" hover-class="none">
        <view class="recmImg">
          <image src="/static/images/2019cfsj_1.png"></image>
        </view>
        <view class="uni-flex-item recmRight">
          <view class="recmrTitle">
            篮球选手球场跌倒，是道德的沦丧还是人性的丧失地方GV额度的深V不懂不懂不服管，都告不到发重新吧不错偷        
          </view>
          <view class="recmrContent">
            篮球选手球场跌倒，地方GV额度的深V不懂不懂不服管，都告不到发重新吧不错偷......         
          </view>
        </view>
      </navigator>
    </view> 
  </view> 
</template>
<script>
  export default{
    data(){
      return{
        
      }
    },
    components:{
      
    }
  }
</script>

<style lang="scss" scoped>
  
  .swiperBox{
    padding: 10rpx 20rpx 20rpx;
    .swiper{
      height:250rpx;
      border-radius:10rpx;
      overflow:hidden;
    }
  }
  
  .category{
    padding:20rpx;
    background:#FFFFFF;
    .cateItem{
      display:flex;
      flex-direction: column;
      justify-content:center;
      align-items:center;
      .cateImg{
        width:80rpx;
        height:80rpx;
        margin-bottom:8rpx;
      }
    }
  }
  .recommendBox{
    padding: 0 20rpx 20rpx;
    background:#FFFFFF;
    .recmTitle{
      padding-left:20rpx;
      font-size:32rpx;
      color:#333333;
      font-weight:400;
      position:relative;
      &::after{
        position: absolute;
        top:0;
        left:0;
        bottom:0;
        content:'';
        width:8rpx;
        height:30rpx;
        background:#FF3333;
        margin:auto;
        border-top-right-radius:10rpx;
        border-bottom-right-radius:10rpx;
      }
    }
    .recmItem{
      align-items:stretch;
      margin-top:24rpx;
      .recmImg{
        width:200rpx;
        height:150rpx; 
        margin-right:12rpx;
        border-radius:10rpx;
        overflow:hidden;
        
      }
      .recmRight{
        overflow: hidden;
      }
      .recmrTitle{
        font-size:28rpx;
        line-height:34rpx;
        font-weight:600;
        margin:10rpx 0;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space:nowrap;
      }
      .recmrContent{
        font-size:22rpx;
        line-height:30rpx;
        color:#999999;
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        -webkit-box-orient: vertical;
         word-break: break-all;
      }
    }
  }
</style>
