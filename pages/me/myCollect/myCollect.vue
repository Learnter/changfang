<template>
	<view class="tabs">
		<view class="searchBox uni-inline-item">
		  <view class="location">东莞<uni-icon type="arrowdown" color="#999999" size="20"></uni-icon></view>
      <view class="searchInpute uni-inline-item">
       <uni-icon  type="search" color="#999999" size="20"></uni-icon> 
       <text class="uni-ellipsis uni-flex-item">搜索你想要的店铺位置或者店铺</text>
      </view>
		</view>
	</view>
</template>

<script>
  
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
	export default {
		data() {
			return {
			
			};
		},
    components:{
      uniIcon
    }
	}
</script>

<style lang="scss" scoped>
  .searchBox{
    margin:16rpx;
    padding:10rpx 20rpx;
    background:#FFFFFF;
    border-radius:40rpx;
    .location{
      padding:0rpx 20rpx;
      font-size:32rpx;
      position:relative;
      &::after{
        position:absolute;
        top:0;
        right:0;
        bottom:0;
        content:'';
        background:#999999;
        width:3rpx;
        height:35rpx;
        margin:auto;
      }
    }
    .searchInpute{
      flex:1;
      padding:0 30rpx;
      text-overflow: ellipsis;
      white-space:nowrap;
      overflow:hidden;
      color:#999999;
      font-size:24rpx;
    }
  }
  
</style>
