<template>
  <view>
    <view class="searchBox uni-inline-item">
      <view class="location uni-inline-item">
        <view class="text2">东莞</view><text class="iconfont icondown"></text></view>
      <view class="searchInpute uni-inline-item">
       <uni-icon  type="search" color="#999999" size="40"></uni-icon> 
       <text class="uni-ellipsis uni-flex-item">搜索你想要的店铺位置或者店铺</text>
      </view>
    </view>
    
    <view class="filterBox uni-inline-item">
      <view class="uni-flex-item uni-inline-item uni-flex-center">
        <view class="text2">区域<text class="iconfont icondown-fill-xs"></text></view>
      </view>
      <view class="uni-flex-item uni-inline-item uni-flex-center">
         <view class="text2">面积<text class="iconfont icondown-fill-xs"></text></view>
      </view>
      <view class="uni-flex-item uni-inline-item uni-flex-center">
        <view class="text2">租金<text class="iconfont icondown-fill-xs"></text></view>
      </view>
    </view>
    
    <view class="listBox">
     <view class="listItem" v-for="(item,index) in 5" :key="index">
        <view class="itemlocation">鑫隆国际A栋802</view>
        <view class="itemImg">
          <image src="/static/images/2019cfsj_1.png"></image>
        </view>
        <view class="itemBottom uni-inline-item itemlocation">
          <view class="uni-flex-item uni-column-item">
            <view class="">租金</view>
            <view class="text1">20000元/月</view>
          </view>
          <view class="uni-flex-item uni-column-item">
            <view class="">面积</view>
            <view class="text1">120㎡</view>
          </view>
          <view class="uni-flex-item uni-column-item">
            <view class="">转让费</view>
            <view class="text1">15万</view>
          </view>
        </view>
      </view>
      <view class="emptybg" v-if="isEmpty">
        <image src="/static/images/2019cfsj_39.png" ></image>
      </view> 
    </view>
  </view> 
</template>

<script>
	import uniIcon from '@/components/uni-icon/uni-icon.vue';
	export default {
		data() {
			return {
			isEmpty:false
			};
		},
	  components:{
	    uniIcon
	  }
	}
</script>

<style lang="scss" scoped>
  
  .icondown{
    margin-left:5rpx;
    color:#999999;
  }
  
  .icondown-fill-xs{
    margin-left:10rpx;
    color:#333333;
    font-weight: 400;
  }
  
   /*搜索框样式*/
   .searchBox{
     margin:16rpx;
     padding:8rpx 20rpx;
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
     /*搜索框样式*/
     .filterBox{
       box-sizing:border-box;
       height:88rpx;
       background:#FFFFFF;
       padding:20rpx;
       box-shadow:0px 1px 0px 0px rgba(0, 0, 0, 0.1);
     }  
    /*条件选择框*/
    
    /*列表框样式*/
    .listBox{
      padding:16rpx 16rpx 0;
      display:flex;
      flex-wrap:wrap;
      .listItem{
        box-sizing:border-box;
        width:50%;
        &:nth-child(odd){
          padding: 0 8rpx 16rpx 0;
        }
        &:nth-child(even){
          padding:0 0 16rpx 8rpx;
        }
      }
    }
    
    .itemlocation{
      padding:10rpx 20rpx;
      background:#F1F1F1;
      border-radius:6rpx;
      white-space:nowrap;
      overflow:hidden;
      text-overflow:ellipsis;
    }
    
    .itemImg{
      width:100%;
      height:200rpx;
      overflow:hidden;
    }
    
    
    .text1{
      font-size:20rpx;
      color:#BC241C;
      overflow:hidden;
      white-space:nowrap;
      text-overflow:ellipsis;
      font-weight:bold;
    }
    
    .text2{
      font-weight:bold;
      margin-right:10rpx;
    }
    /*列表框样式*/
    
    /*空列表背景*/
    .emptybg{
      width:400rpx;
      height:300rpx;
      margin:200rpx auto;
    }  
      
      
</style>
