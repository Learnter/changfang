<template>
	<view class="content">
		<view class="uni-inline-item uni-flex-between">
		  <text class="askTitle">猜你想问</text>
      <view class="serviceImg">
        <image src="/static/images/2019cfsj_66.png" mode=""></image>
      </view>
		</view>
    
    <view class="aboutWithDraw">
      <view class="aboutTitle">关于提现</view>
      <view class="askItem">
        <view class="">1.提现时间是多久?</view>
        <view class="uni-h5 aboutWord">提现审核时间一般为二十四的小时，提现资金将在四十八小时内到账</view>
      </view>
      <view class="askItem">
        <view class="">2.提现金额没有到账?</view>
        <view class="uni-h5 aboutWord">提现金额没有到账也许是账号出现异常，或者此订单的审核未通过</view>
      </view>
      <view class="askItem">
        <view class="">3.无法提现?</view>
        <view class="uni-h5 aboutWord">无法提现可能是该账户已经被冻结，或者提现金额过大，账户余额不足等原因</view>
      </view>
    </view>
    
    <view class="aboutWithDraw">
        <view class="aboutTitle">关于充值</view>
      <view class="askItem">
        <view class="">1.金额过小不能充值?</view>
        <view class="uni-h5 aboutWord">本平台充值金额最小不得小于10元。充值时选择金额必须选择等于10或者是10的倍数</view>
      </view>
      <view class="askItem">
        <view class="">2.无法充值?</view>
        <view class="uni-h5 aboutWord">无法充值可能是该账户已经被冻结，或者充值所绑定的银行卡余额不足</view>
      </view>
    </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss" scoped>
 .content{
   box-sizing:border-box;
   width:100%;
   height:100%;
   padding:20rpx 20rpx 0;
 }
 
 .askTitle{
   font-size:32rpx;
   font-weight:bold;
   color:#343434;
 }
 
 .serviceImg{
   width:60rpx;
   height:60rpx;
   background: red;
   border-radius:50%;
 }
 
 .aboutWithDraw{
   border-bottom:1rpx solid #D9D9D9;
 }
 
 .aboutTitle{
   color:#343434;
   font-size:30rpx;
   padding:20rpx 0;
 }
   
 .aboutWord{
   padding-left:20rpx;
   position:relative;
   line-height:40rpx;
   &::before{
     content:'';
     position:absolute;
     left:4rpx;
     top:16rpx;
     width:6rpx;
     height:6rpx;
     background:#999999;
     border-radius:50%;
   }
 }
 
 .askItem{
   margin-bottom:30rpx;
 }
</style>
