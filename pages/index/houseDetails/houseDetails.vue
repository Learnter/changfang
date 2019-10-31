<template>
	<view style="margin-bottom:100rpx;">
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
    
    <view class="transferBox">
      <view class="uni-inline-item uni-flex-between" style="padding: 0 30rpx 10rpx">
        <view class="uni-column-item">
          <view class="text1">租金</view>
          <view class="text1" style="color:#B91B12">2000元/月</view>
        </view>
        <view class="uni-column-item">
          <view class="text1">面积</view>
          <view class="text1" style="color:#B91B12">120㎡</view>
        </view>
        <view class="uni-column-item">
          <view class="text1">转让费</view>
          <view class="text1" style="color:#B91B12">15万</view>
        </view>
      </view>
      <view class="">区域：东莞市-南城</view>
      <view class="">地址：南城中心财富大楼对面</view>
    </view>
    
    <view class="transferBox">
      <view class="headTitle">铺源信息</view>
      <view>
        <view class="">当前经营：日常办公场所</view>
        <view class="">位置信息：东莞-南城</view>
        <view class="">月 租 金：2000元/月</view>
        <view class="">最长租期：12月</view>
        <view class="">转账费用：15万</view>
      </view>
    </view>
    
    <view class="transferBox">
      <view class="headTitle">业主介绍</view>
      <view class="uni-inline-item uni-flex-between">
        <view class="uni-inline-item ownerInfo">
          <view class="ownerImg">
            <image src="/static/images/2019cfsj_11.png"></image>
          </view>
          <view class="">何先生</view>
        </view>
        <uni-icon type="phone-filled" color="#2EC788" size="28"></uni-icon>
      </view>
      <view class="ownerMsg">
        一.生意人，每天把他的店铺收拾得干干净净，东西分类摆
        放得整整齐齐，只要你说出买什么，他能准确找到东西的
        二.位置，价钱合理，不坑蒙拐骗，早晨早早到店铺，晚上
        很晚才回家，非常敬业，如果你要的东西没有，他会道歉，
        并回答可以给你尽快进货              
      </view>
    </view>
    
    <view class="transferBox">
      <view class="headTitle">常见问题</view>
      <view>
        <view class="uni-inline-item uni-flex-between" style="margin-bottom:10rpx" v-for="(item,index) in 5" :key="index">
          <view class="uni-inline-item">
            <view class="bedge">1</view>
            <text>怎么找到好的铺源</text>
          </view>
          <uni-icon type="arrowright" color="#000000"  size="18"></uni-icon>
        </view>
      </view>
    </view>
    
    <view class="bottomBox uni-inline-item">
      <view class="uni-inline-item btItem" @click="$refs['share'].open()">
        <uni-icon type="location" color="#ffffff" size="20"></uni-icon>
        海报
      </view>
      <view class="uni-inline-item btItem">
        <uni-icon type="location-filled" color="#ffffff" size="20"></uni-icon>
         定位
      </view>
      <view class="uni-inline-item btItem">
        <uni-icon type="chat" color="#ffffff" size="20"></uni-icon>
        在线聊天
      </view>
      <view class="uni-inline-item btItem">
        <uni-icon type="phone-filled" color="#ffffff" size="20"></uni-icon>
        直拨店主
      </view>
    </view>
    
    
    <!-- 底部分享弹窗 -->
    <uni-popup ref="share" type="bottom" :custom="true">
    	<view class="uni-share" >
    		<view class="uni-share-title">分享到</view>
    		<view class="uni-share-content">
    			<view v-for="(item, index) in bottomData" :key="index" class="uni-share-content-box">
    				<view class="uni-share-content-image">
    					<image :src="item.icon" class="image" />
    				</view>
    				<view class="uni-share-content-text">{{ item.text }}</view>
    			</view>
    		</view>
    		<view class="uni-share-btn" @click="cancel('share')">取消分享</view>
    	</view>
    </uni-popup>
	</view>
</template>

<script>
  import uniSwiperDot from '@/components/uni-swiper-dot/uni-swiper-dot.vue';
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
  import uniPopup from '@/components/uni-popup/uni-popup.vue';
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
        bottomData: [{
        		text: '微信',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-2.png',
        		name: 'wx'
        	},
        	{
        		text: '支付宝',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-8.png',
        		name: 'wx'
        	},
        	{
        		text: 'QQ',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/gird-3.png',
        		name: 'qq'
        	},
        	{
        		text: '新浪',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-1.png',
        		name: 'sina'
        	},
        	{
        		text: '百度',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-7.png',
        		name: 'copy'
        	},
        	{
        		text: '其他',
        		icon: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-5.png',
        		name: 'more'
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
      },
      cancel(type) {
      	if (type === 'tip') {
      		this.show = false
      		return
      	}
      	this.$refs[type].close()
      },
      // shareBtn(){
      //   
      // }
    },
    components:{
      uniSwiperDot,
      uniIcon,
      uniPopup
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
  
  .transferBox{
    padding:20rpx;
    background:#FFFFFF;
    margin-bottom:10rpx;
  }
  
  .headTitle{
    font-size:32rpx;
    font-weight: bold;
    text-align:center;
    position:relative;
    padding:10rpx 0;
    margin-bottom:20rpx;
    &::after{
      content:'';
      position:absolute;
      left:0;
      top:100%;
      right:0;
      background:#B91B12;
      width:100rpx;
      height:4rpx;
      overflow:hidden;
      margin:auto;
    }
  }
  
  .ownerImg{
    width:100rpx;
    height:100rpx;
    border-radius:50%;
    overflow:hidden;
    margin-right:30rpx;
  }
  
  .ownerMsg{
    background:#F0F2F1;
    font-size:26rpx;
    color:#999999;
    border-radius:10rpx;
    letter-spacing:2rpx;
    padding:20rpx;
    margin:20rpx 0 30rpx;
  }
  
  .text1{
    font-size:30rpx;
    font-weight:bold;
  }
  
  .bedge{
    width:40rpx;
    height:40rpx;
    line-height:40rpx;
    border-radius:50%;
    background:#B91B12;
    color:#FFFFFF;
    text-align:center;
  }
  
  .bottomBox{
    position:fixed;
    left:0;
    right:0;
    bottom:0;
    height:100rpx;
    background:#FFFFFF;
    box-shadow: 0 -1rpx 5rpx #C0C0C0;
  }
  
  .btItem{
    color:#FFFFFF;
     justify-content:center;
    &:nth-child(1){
      width:20%;
      height:100%;
      background:#F42C2E;
    }
    &:nth-child(2){
      width:20%;
      height:100%;
      background:#FBA51E;
    }
    &:nth-child(3){
      width:30%;
      height:100%;
      background:#EE9CA2;
    }
    &:nth-child(4){
      width:30%;
      height:100%;
      background:#F42C2E;
    }
  }
  
  
  /* 底部分享 */
  .uni-share {
  	background: #fff;
  }
  
  .uni-share-title {
  	line-height: 60upx;
  	font-size: 24upx;
  	padding: 15upx 0;
  	text-align: center;
  }
  
  .uni-share-content {
  	display: flex;
  	flex-wrap: wrap;
  	padding: 15px;
  }
  
  .uni-share-content-box {
  	display: flex;
  	flex-direction: column;
  	align-items: center;
  	width: 25%;
  	box-sizing: border-box;
  }
  
  .uni-share-content-image {
  	display: flex;
  	justify-content: center;
  	align-items: center;
  	width: 60upx;
  	height: 60upx;
  	overflow: hidden;
  	border-radius: 10upx;
  }
  
  .uni-share-content-image .image {
  	width: 100%;
  	height: 100%;
  }
  
  .uni-share-content-text {
  	font-size: 26upx;
  	color: #333;
  	padding-top: 5px;
  	padding-bottom: 10px;
  }
  
  .uni-share-btn {
  	height: 90upx;
  	line-height: 90upx;
  	border-top: 1px #f5f5f5 solid;
  	text-align: center;
  	color: #666;
  }

</style>
