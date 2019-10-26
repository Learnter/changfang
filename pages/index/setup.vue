<template>
	<view class="content">
		<view class="eyitopBox" >
			<view class="eyitopbgg"></view>
			<view class="eyitopCont">
				<!-- <view class="eyitopqdao uni-flex">
					<image src="../../static/images/2019cfsj_49.png" mode=""></image>
					<view class="fx1 eyitopqdaotx">签到</view>
				</view>
				<view class="uni-flex">
					<view class="eyitotximg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="eyitodata fx1">
						<view class="eyitodatatx">
							<text class="text_1">手机认证：182****2345</text>
							<text class="text_2">[ 已认证 ]</text>
						</view>
						<navigator class="eyitodatalink" url="/pages/me/editInfo/editInfo" hover-class="none">编辑资料</navigator>
					</view>
				</view -->
        <image src="/static/images/2019cfsj_66.png" ></image>
			</view>
		</view>
		<view class="eyinlinkoneBox">
      <view class="eyinlinkoneHe">
         <view class="eyinlinkonetop">
           <view class="uni-inline-item textColor">
             <text>请设定昵称</text>
             <navigator class="editImg" url="/pages/me/editInfo/editInfo" hover-class="none">
               <image src="/static/images/2019cfsj_65.png" mode=""></image>
             </navigator>
           </view>
           <view class="textColor">
             ID:-----
           </view>
           <view class="accountlogo">
             <image src="/static/images/2019cfsj_11.png"></image>
           </view>
         </view>
         <view class="uni-flex">
         	<view class="fx1 eyinlinkonedh">
         		<view class="eyinlinkonedhimg">201.25</view>
         		<view class="eyinlinkonetx">累积收益</view>
         	</view>
         	<view class="fx1 eyinlinkonedh">
         		<view class="eyinlinkonedhimg">0.12</view>
         		<view class="eyinlinkonetx">账户余额</view>
         	</view>
         	<view  class="fx1 eyinlinkonedh">
         		<view class="eyinlinkonedhimg">0.00</view>
         		<view class="eyinlinkonetx">可用积分</view>
         	</view>
         </view>
         <view class="uni-inline-item signBox">
           <view class="moneyImg">
             <image src="/static/images/2019cfsj_49.png"></image>
           </view>
           <view>签到领积分</view>
         </view>
      </view>
		</view>
    
    <view class="actionBox uni-inline-item">
      <view class="acItem uni-inline-item">
          <view class="aciImg">
            <image src="/static/images/2019cfsj_67.png" mode=""></image>
          </view>
          <text>充值</text>
      </view>
      <view class="acItem uni-inline-item">
         <view class="aciImg">
          <image src="/static/images/2019cfsj_68.png" mode=""></image>
         </view>
         <text>提现</text>
      </view>
    </view>
    
		<view class="eyinlinkoneBox">
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_50.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">我的收藏</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_51.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">客服留言</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_52.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">我的资料</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_53.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">我要投诉</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_54.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">我要提意见</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
			<navigator url="#" class="eylinktwoBox uni-flex" hover-class="none">
				<view class="eylinktwoimg">
					<image src="../../static/images/2019cfsj_55.png" mode=""></image>
				</view>
				<view class="eylinkttxt fx1">帮助中心</view>
				<view class="eylinkzxia"><uni-icon type="arrowright" color="#888888" size="18"/></view>
			</navigator>
		</view>
    
  <view class="messageBox" :class="showMessage == true ? 'messageActive':''" @touchmove.stop.prevent="">
      <view class="messagelist">
        <scroll-view scroll-y  style="height:100%"  >
          <view class="msItem uni-flex" v-for="(item,index) in 6" :key="index">
            <view class="uni-flex-item">
              <view class="msi_content">
                厂房在线上限了！快快看新上了什么新功能吧天使的翅膀洗洗弄弄系兄弟家
              </view>
              <view class="msi_time uni-flex">
                <text>2019年10月23日</text>
                <text class="msi_status">查看</text>
              </view>
            </view>
            <view class="bedge"></view>
          </view>
        </scroll-view>
        <view class="messageTitle">
           <image src="/static/images/2019cfsj_62.png"></image>
           <text class="titleWord">我的消息</text>
        </view>
        <view class="close" @tap="showMessage = false">
           <uni-icon type="close" size="35" color="#FFFFFF"></uni-icon>
        </view>
        
        <view class="itemDetail">
          
        </view>
      </view> 
    </view>
	</view>
</template>

<script>
  import uniIcon from '@/components/uni-icon/uni-icon.vue'
  import uniBadge from '@/components/uni-badge/uni-badge.vue'
	export default {
		data() {
			return {
				showMessage:false
			}
		},
		onLoad() {
	
		},
		methods: {
		},  
    components:{
      uniIcon,
      uniBadge
    }
	}
</script>

<style lang="scss" scoped>
  
  page,.content{
    width:100%;
    height:100%;
    overflow-y:scroll;
  }
  
	.eyitopBox {
		position:relative;
    display:flex;
    justify-content: flex-end;
	}
  
	.eyitopbgg {
		position: absolute;
		z-index: 10;
    left:0;
    right:0;
    top:0;
		height:300rpx;
    background: linear-gradient(to right,#FE0F32,#DC0127);
		// background: -webkit-linear-gradient(left, #C33B33, #A11911);
		// background: -o-linear-gradient(left, #C33B33, #A11911);
		// background: -moz-linear-gradient(left, #C33B33, #A11911);
		// background: linear-gradient(left, #C33B33, #A11911);
	}
	.eyitopCont {
		position: relative;
		z-index: 100;
    padding:30rpx 20rpx;
    width:80rpx;
    height:80rpx;
    /* #ifdef H5 */
    box-sizing:content-box;
    /* #endif */
	}
	.eyitopqdao {
		position: absolute;
		top:30rpx;
		right:0rpx;
		background: #D08C88;
		padding: 10rpx;
		border-radius: 30rpx 0rpx 0rpx 30rpx;
	}
	.eyitopqdao image {
		width: 35rpx;
		height: 35rpx;
	}
	.eyitopqdaotx {
		line-height: 35rpx;
		min-width: 80rpx;
		text-align: center;
		padding: 0rpx 5rpx;
		color: #ffffff;
		font-size: 26rpx;
	}
	.eyitotximg {
		width: 120rpx;
		height: 120rpx;
		border-radius: 50%;
		overflow: hidden;
		background: #ffffff;
	}
	.eyitotximg image {
		width: 100%;
		height: 100%;
	}
	.eyitodata {
		padding:15rpx 20rpx 0rpx 20rpx;
	}
	.eyitodatatx .text_1 {
		color: #ffffff;
		font-size: 26rpx;
		margin-right: 8rpx;
	}
	.eyitodatatx .text_2 {
		color: #FCDB2C;
		font-size: 26rpx;
	}
	.eyitodatalink {
		color: #FCDB2C;
		font-size: 26rpx;
	}
	.eyinlinkoneBox {
		padding: 0rpx 15rpx 15rpx 15rpx;
		position: relative;
		z-index: 120;
	}
	.eyinlinkoneHe {
		box-shadow: 0rpx 2rpx 10rpx #dddddd;
		background: #ffffff;
		padding: 20rpx 30rpx 30rpx;
		border-radius: 10rpx;
    position:relative;
	}
	.eyinlinkonedh {
		text-align: center;
	}
	.eyinlinkonedhimg {
		font-size:32rpx;
    color:#FC7400;
    font-weight:600;
	}
	.eyinlinkonetx {
		color: #333333;
		font-size:32rpx;
    font-weight:700;
	}
	.eylinktwoimg {
		min-width:70rpx;
		height:45rpx;
		line-height:45rpx;
	}
	.eylinktwoimg image {
		width: 45rpx;
		height: 45rpx;
	}
	.eylinkttxt {
		height:45rpx;
		line-height:45rpx;
	}
	.eylinkzxia {
		height:45rpx;
		line-height: 45rpx;
	}
	.eylinktwoBox {
		padding: 30rpx 10rpx 30rpx 25rpx;
		border-radius: 5rpx;
		box-shadow: 0rpx 2rpx 10rpx #eeeeee;
		margin-top: 15rpx;
	}
  
  /*头像框样式*/
  .eyinlinkonetop{
     position:relative;
     padding-left:200rpx; 
     margin-bottom:20rpx;
     .textColor{
       font-size:32rpx;
       color:#9E9E9E;
     }
     .editImg{
       width:40rpx;
       height:40rpx;
     }
     .accountlogo{
       position:absolute;
       left:0;
       bottom:0;
       width:170rpx;
       height:170rpx;
       border-radius:50%;
       border:6rpx solid #FFE799;
       overflow:hidden;
    }
  } 
  /*头像框样式*/
  
  /*签到样式*/
  .signBox{
    position:absolute;
    right:0;
    top:30rpx;
    padding:10rpx;
    background:#FBDEDC;
    border-radius:40rpx 10rpx 10rpx 40rpx;
    font-size:26rpx;
    .moneyImg{
      width:40rpx;
      height:40rpx;
      margin-right:10rpx;
    }
  }
  /*签到样式*/
  
  /*充值,提现样式*/
  .actionBox{
    padding:20rpx 20rpx;
    justify-content:space-between;
    .acItem{
      padding:10rpx 0;
      align-items:center;
      font-size:36rpx;
      font-weight:500;
      color:#FFFFFF;
      justify-content:center;
      .aciImg{
        width:50rpx;
        height:50rpx;
      }
      &:nth-child(1){
        width:47%;
        border-radius:50rpx;
        background: linear-gradient(to right,#FF6548,#FC444D);
      }
      &:nth-child(2){
        width:47%;
        background: linear-gradient(to right,#FEC500,#FCB600);
        border-radius:50rpx;
      }
    }
    
  }  
  /*充值,提现样式*/
  
  /*消息框*/
  .messageBox{
    position:fixed;
    left:0;
    right:0;
    top:0;
    bottom:0;
    visibility:hidden;
    .messagelist{
      position:absolute;
      left:50%;
      top:50%;
      transform: translate(-50%,-50%);
      background:#FFFFFF;
      width:600rpx;
      height:800rpx;  
      border-radius:20rpx;
      padding:40rpx 20rpx 30rpx;
      box-shadow: 0 0 20rpx #333333;
      .itemDetail{
        position:absolute;
        left:0;
        top:0;
        right:0;
        bottom:0;
      }
      .msItem{
        background:#F6F6F6;
        margin-bottom:20rpx;
        border-radius:10rpx;
        padding:20rpx;
        .bedge{
          margin-left:20rpx;
          margin-top:10rpx;
          width:20rpx;
          height:20rpx;
          background:#FF0000;
          border-radius:50%;
        }
        .msi_content{
          height:90rpx;
          line-height:45rpx;
          font-size:32rpx;
          letter-spacing:4rpx;
          font-family:SimHei;
          font-weight:bold;
          overflow: hidden;
          text-overflow: ellipsis;
          display: -webkit-box;
          -webkit-line-clamp:2;  /* 设置行数 */
          -webkit-box-orient: vertical;
        }
        .msi_time{
          margin-top:20rpx;
          justify-content:space-between;
          color:#999999;
          .msi_status{
            color:#3888FF;
          }
        }
      }
    }
    .messageTitle{
      position:absolute;
      left:50%;
      transform:translateX(-50%);
      top:-11%;
      width:70%;
      height:130rpx;
      .titleWord{
        position:absolute;
        left:50%;
        top:65%;
        transform:translate(-50%,-50%);
        font-size:32rpx;
        letter-spacing:10rpx;
        color:white;
      }
    }
    .close{
      position: absolute;
      left:50%;
      transform:translateX(-50%);
      top:103%;
    }
  }
  
  .messageActive{
    background:rgba(0,0,0,0.5);
    visibility: visible;
    z-index:999;
  }
	/*消息框*/
</style>
