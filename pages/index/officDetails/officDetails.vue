<template>
	<view>
    <uni-swiper-dot :info="info" :current="current" mode="nav" :dots-styles="dotsStyles" field="content">
    	<swiper class="swiper-box" @change="change">
    		<swiper-item v-for="(item, index) in info" :key="index">
    			<view :class="item.colorClass" class="swiper-item">
    				<image :src="item.url" mode="aspectFill" />
    			</view>
    		</swiper-item>
    	</swiper>
    </uni-swiper-dot>
    
    <view class="baseBox">
      <view class="baseInfo">东莞市南城中心 世纪大厦 办公室招租就看必胜客吗</view>
      <view class="uni-inline-item uni-flex-between">
        <view class="uni-inline-item baseAction">
          <uni-icon type="star"></uni-icon>
          <view class="actionText">分享</view>
        </view>
        <view class="uni-inline-item baseAction">
          <uni-icon type="star"></uni-icon>
          <view class="actionText">立即联系</view>
        </view>
        <view class="uni-inline-item baseAction">
          <uni-icon type="star"></uni-icon>
          <view class="actionText">收藏</view>
        </view>
        <view class="uni-inline-item baseAction">
          <uni-icon type="star"></uni-icon>
          <view class="actionText">纠错</view>
        </view>
      </view>
    </view>
    
    <view class="introduceBox">
      <view class="intr_title">写字楼介绍</view>
      <view class="intr_content">
        隆鑫国际位于虎门镇北栅东坊一路深水区净，旁边两座碧
        桂圆整整齐齐，只要你说出买什么，他能准确找到东西的
        二.位置，价钱合理，不坑蒙拐骗，早晨早早到店铺，晚上
        很晚才回家，非常敬业，如果你要的东西没有，他会道歉，
        并回答可以给你尽快进货          
      </view>
    </view>
    
    <view class="correlationBox">
      <view class="uni-inline-item watchMore">
        <view class="wordStyle">相关出租</view>
        <view class="uni-inline-item wordStyle2">
          更多<uni-icon type="arrowright" color="#999999"></uni-icon>
        </view>
      </view>
      <view class="uni-flex uni-row-wrap listBox">
        <view class="outItem" v-for="(item,index) in 4" :key="index">
          <view class="insideItem">
            <view class="itemAddress">鑫隆国际A栋802</view>
            <view class="jzhochptimg">
            	<image src="/static/images/2019cfsj_6.png" ></image>
            </view>
            <view class="uni-inline-item itemBottom">
              <view class="uni-column-item">
                <view class="textStyle">租金</view>
                <view class="redColor">2000元/月</view>
              </view>
              <view class="uni-column-item">
                <view class="textStyle">面积</view>
                <view class="redColor">120㎡</view>
              </view>
              <view class="uni-column-item">
                <view class="textStyle">转让费</view>
                <view class="redColor">15万</view>
              </view>
            </view>
          </view>
        </view>
      </view>
    </view>
	</view>
</template>

<script>
  import uniSwiperDot from '@/components/uni-swiper-dot/uni-swiper-dot.vue';
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
	export default {
		data() {
			return {
				info: [{
						colorClass: 'uni-bg-red',
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/shuijiao.jpg',
						content: '内容 A'
					},
					{
						colorClass: 'uni-bg-green',
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/muwu.jpg',
						content: '内容 B'
					},
					{
						colorClass: 'uni-bg-blue',
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/cbd.jpg',
						content: '内容 C'
					}
				],
				dotStyle: [{
						backgroundColor: 'rgba(0, 0, 0, .3)',
						border: '1px rgba(0, 0, 0, .3) solid',
						color: '#fff',
						selectedBackgroundColor: 'rgba(0, 0, 0, .9)',
						selectedBorder: '1px rgba(0, 0, 0, .9) solid'
					},
					{
						backgroundColor: 'rgba(255, 90, 95,0.3)',
						border: '1px rgba(255, 90, 95,0.3) solid',
						color: '#fff',
						selectedBackgroundColor: 'rgba(255, 90, 95,0.9)',
						selectedBorder: '1px rgba(255, 90, 95,0.9) solid'
					},
					{
						backgroundColor: 'rgba(83, 200, 249,0.3)',
						border: '1px rgba(83, 200, 249,0.3) solid',
						color: '#fff',
						selectedBackgroundColor: 'rgba(83, 200, 249,0.9)',
						selectedBorder: '1px rgba(83, 200, 249,0.9) solid'
					}
				],
				modeIndex: -1,
				styleIndex: -1,
				current: 0,
        dotsStyles:{}
			};
		},
    methods:{
      change(e) {
      	this.current = e.detail.current
      }
    },
    components:{
      uniSwiperDot,
      uniIcon
    }
	}
</script>

<style lang="scss" scoped>
  
  .swiper-box {
  	height: 500rpx;
  }
  
  .swiper-item {
  	display: flex;
  	justify-content: center;
  	align-items: center;
  	height: 100%;
  	background: #eee;
  	color: #fff;
  }
  
  .swiper-item image {
  	width: 100%;
  	height: 100%;
  }
  
  .baseBox{
    padding:20rpx;
    background:#FFFFFF;
    margin-bottom:10rpx;
    .baseInfo{
      line-height:45rpx;
      color:#000000;
      font-weight:bold;
      font-size:32rpx;
      margin-bottom:10rpx;
      overflow:hidden;
      display:-webkit-box;
      text-overflow:ellipsis;
      -webkit-line-clamp:2;
      -webkit-box-orient:vertical;
    }
    .baseAction{
      justify-content: center;
      .actionText{
        font-size:24rpx;
        color:#999999;
      }
    }
  }
  
  
  .introduceBox{
    padding:20rpx;
    background:#FFFFFF;
    margin-bottom:10rpx;
    border-radius:10rpx;
    .intr_title{
      text-align:center;
      font-size:32rpx;
      font-weight:bold;
      margin-bottom:10rpx;
    }
    .intr_content{
      padding:20rpx;
      background:#F0F2F1 ;
      border-radius:16rpx;
      line-height:40rpx;
      color:#999999;
      font-size:26rpx;
    }
  }
  
  .correlationBox{
    background:#FFFFFF;
    padding-bottom:20rpx;
    .watchMore{
      padding:8rpx 20rpx 0;
      justify-content:space-between;
    }
    .listBox{
      padding:6rpx;
      .outItem{
        box-sizing: border-box;
        width:50%;
        padding:6rpx;
        background:#FFFFFF;
        .insideItem{
          background:#F3F3F3;
          border-radius:10rpx;
        }
      }
    }
  }
  
  .textStyle{
    font-size:26rpx;
    font-weight:bold;
  }
  
  .redColor{
    font-size:22rpx;
    color:#BC241C;
    font-weight:bold;
  }
  
  .jzhochptimg {
  	width: 100%;
  	height: 220rpx;
  	overflow: hidden;
  }
  
  .itemAddress{
    padding:10rpx;
    color:#333333;
  }
  
  .itemBottom{
    padding:10rpx 16rpx;
    justify-content:space-between;
  }
  
  .wordStyle{
    font-size:30rpx;
    color:#000000;
    font-weight:bold;
    padding-left:20rpx;
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
      border-top-right-radius:6rpx;
      border-bottom-right-radius:6rpx;
    }
  }
  
  .wordStyle2{
    font-size:24rpx;
    color:#999999;
    font-weight:400;
  }
</style>
