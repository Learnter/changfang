<template>
	<view class="content">
		<view class="accountBox">
		  <view class="accountInfo">
		    <view class="uni-inline-item uni-flex-between accountText">
		      <text>账户余额（元）</text>
          <text class="iconfont iconxunwen"></text>
		    </view>
        <view class="accountNum">100.00</view>
        <view class="uni-inline-item uni-flex-between">
          <view class="uni-inline-item bankInfo">
           <text>中国银行</text>
           <view class="splitline"></view>
           <text>6254 **** **** 2536</text>
           <text class="iconfont iconbinaji"></text>
          </view>
          <view class="uni-inline-item withdrawBtn">
            <text class="iconfont icontixian"></text>
            <text class="">提现</text>
          </view>
        </view>
		  </view>
		</view>
    
    <scroll-view class="logBox" scroll-y="true" @scrolltolower="loadMore">
      <view class="logItem" v-for="(item,index) in 10" :key="index">
        <view class="itemName">我是用户</view>
        <view class="itemTime">2019-08-23 20:05:02</view>
        <view class="itemMoney">300</view>
      </view>
      <view class="example-body" v-show="loadmore">
      	<uni-load-more :status="status" :content-text="contentText"/>
      </view>
    </scroll-view>
	</view>
</template>

<script>
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
  import uniLoadMore from '@/components/uni-load-more/uni-load-more.vue'
	export default {
		data() {
			return {
         loadmore:false,
				 status: 'more',
					contentText: {
						contentdown: '查看更多',
						contentrefresh: '加载中...',
						contentnomore: '没有更多'
					}
			}
		},
    methods:{
      loadMore(e){
        this.loadmore = true;
        this.status = "more";
      }
    },
    components:{
      uniIcon,
      uniLoadMore
    }
	}
</script>

<style lang="scss" scoped>
  
  .iconxunwen{
    font-size:50rpx;
  }
   
  .iconbinaji{
    font-size:40rpx;
    margin-left:20rpx;
  }
  
  .icontixian{
    color:#FE2549;
    margin-right:4rpx;
  }
  
  .content{
    width:100%;
    height:100%;
  }
  
  .accountBox{
    box-sizing:border-box;
    width:100%;
    height:300rpx;
    background:#FFFFFF;
    padding:20rpx 16rpx 16rpx;
    .accountInfo{
      box-sizing:border-box;
      width:100%;
      height:100%;
      background-image:url('~@/static/images/2019cfsj_101.png');
      background-repeat:no-repeat;
      background-size:cover;
      box-shadow:0px 3px 5px 0px rgba(253,73,76,0.38);
      border-radius:10rpx;
      padding:20rpx 30rpx;
      display:flex;
      flex-direction:column;
      justify-content:space-between;
      .accountText{
        color:#FFFFFF;
        font-size:30rpx;
        line-height: 1.3;
      }
      .accountNum{
        font-size:60rpx;
        font-weight:bold;
        color:#FED100;
      }
      .bankInfo{
        color:#830017;
        font-size:30rpx;
      }
      
      .withdrawBtn{
        background:#FFFFFF;
        padding:0 16rpx;
        border-radius:20rpx;
        line-height: 1.5;
        color:#FE2549;
      }
      .withdrawImg{
        width:30rpx;
        height:30rpx;
        margin-right:10rpx;
      }
    }
  }
  
  .splitline{
    width:5rpx;
    height:30rpx;
    background:#830017;
    margin: 0 20rpx;
  }
  
  .editBank{
    width:35rpx;
    height:35rpx;
  }
  
  .logBox{
    box-sizing:border-box;
    width:100%;
    height:calc(100% - 300rpx);
    padding: 10rpx 20rpx 20rpx;
    .logItem{
      box-sizing:border-box;
      background:#FFFFFF;
      height:130rpx;
      padding:16rpx;
      border-radius:8rpx;
      margin-bottom:16rpx;
      position:relative;
      .itemName{
        font-size:30rpx;
        font-weight:600;
      }
      .itemTime{
        color:#999999;
      }
      .itemMoney{
        position:absolute;
        right:20rpx;
        top:50%;
        transform:translateY(-50%);
        font-size:30rpx;
        font-weight:bold;
      }
    }
  }
  
  
  .example-body{
    position: fixed;
    left:0;
    bottom:0;
    right:0;
    background:#FAFAFA;
    transition: background-color 1s ease-in;
  }
  
  
</style>
