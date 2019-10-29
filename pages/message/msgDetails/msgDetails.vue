<template>
	<view class="content">
		<view class="mainBox">
		  <text class="mainTitle">国内首次！两天特高压直流同时跨越同党500千伏线路</text>
      <view class="mainMsg">今日话题 &nbsp;&nbsp;&nbsp;文|向红艳   2019-11-15 - 08:19:23</view>
      <view class="mainContent">
        
      </view>
		</view>
    <view class="hotspot">
     <view class="hsTitle">推荐热点</view>
     <navigator class="recmItem uni-inline-item" url="/pages/message/msgDetails/msgDetails" v-for="(item,index) in 3" :key="index" hover-class="none">
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
    <view class="commentBox">
      <view class="hsTitle">热门评论</view>
      <view class="uni-flex cmItem" v-for="(item,index) in 3" :key="index">
        <view class="cmi_img">
          <image src="/static/images/2019cfsj_11.png"></image>
        </view>
        <view class="uni-flex-item">
          <view class="uni-inline-item cmi_info">
            <text class="uni-flex-item">热心李先生</text>
            <view class="uni-inline-item">
              <view class="uni-inline-item" style="margin-right:20rpx">
                <uni-icon type="chat"></uni-icon>36
              </view>
              <view class="uni-inline-item">
                <uni-icon type="chat"></uni-icon>10
              </view>
            </view>
          </view>
          <view class="cmi_content">
             我觉得这个主意很不错哎
          </view>
          <view class="cmi_time">
            1小时
          </view>
        </view>
      </view>
    </view>
    <view class="publishBox uni-inline-item">
      <view class="uni-flex-item inputBox" @click="togglePopup">
       说点什么...
      </view>
      <view class="uni-inline-item">
        <view class="uni-inline-item" style="margin-right:20rpx">
          <uni-icon type="chat"></uni-icon>&nbsp;&nbsp;评论
        </view>
        <view class="uni-inline-item">
          <uni-icon type="chat"></uni-icon>&nbsp;&nbsp;点赞
        </view>
      </view>
    </view>
    <uni-popup ref="popup" :type="type">
      <view class="">
        <view class="release">
           <view class="sendBtn" :class="show?'active':''">发送</view>
        </view>
        <textarea @input="changeText" class="areaInput" value="" placeholder="我来说两句..."/>
      </view>
    </uni-popup>
	</view>
</template>

<script>
  import uniPopup from '@/components/uni-popup/uni-popup.vue'
  import uniIcon from "@/components/uni-icon/uni-icon.vue";
	export default {
		data() {
			return {
        type: '',
        show:false
			};
		},
    methods:{
      togglePopup(){
        this.type = "bottom";
        this.$refs['popup'].open();
      },  
      changeText(e){
       if(e.detail.value.trim().length !== 0){
         this.show = true;
       }else{
         this.show = false;
       }
      }
    },
    components:{
      uniIcon,
      uniPopup
    }
	}
</script>

<style lang="scss" scoped>
  
  page,.content{
    width:100%;
    height:100%;
    overflow-y:scroll;
    position:relative;
  }
  
 .mainBox{
   padding:10rpx 20rpx 20rpx;
   background:#FFFFFF;
   margin-bottom:16rpx;
   .mainTitle{
     font-size:38rpx;
     font-weight:bold;
     line-height:50rpx;
     overflow:hidden;
     text-overflow:ellipsis;
     display: -webkit-box;
     -webkit-line-clamp: 2;
     -webkit-box-orient: vertical;
   }
   .mainMsg{
     padding:16rpx 0;
     color:#999999;
     overflow:hidden;
     text-overflow:ellipsis;
     white-space:nowrap;
   }
 }
 
 .hotspot{
   padding:0 20rpx 20rpx;
   background:#FFFFFF;
   margin-bottom:16rpx;
   .hsTitle{
    color:#333333;
    font-size:30rpx;
    font-weight:400;
    padding:10rpx 0;
    border-bottom:1px solid #e4e4e4;
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
       -webkit-line-clamp:3;
       -webkit-box-orient: vertical;
       word-break: break-all;
     }
   }
 }
 
 .commentBox{
   padding:0 20rpx;
   background:#FFFFFF;
   margin-bottom:120rpx;
   .hsTitle{
    color:#333333;
    font-size:30rpx;
    font-weight:400;
    padding:10rpx 0;
    border-bottom:1px solid #e4e4e4;
   }
   .cmItem{
     padding:16rpx 0;
     .cmi_img{
       width:70rpx;
       height:70rpx;
       overflow:hidden;
       border-radius:50%;
       margin-right:20rpx;
     }
     .cmi_info{
       justify-content:space-between;
       font-size:28rpx;
       margin-top:10rpx;
       color: #999999;
     }
     .cmi_content{
       color:#333333;
       font-weight:400;
       font-size:26rpx;
       line-height:40rpx;
       letter-spacing:2rpx;
       overflow: hidden;
       text-overflow: ellipsis;
       display: -webkit-box;
       -webkit-line-clamp:2;
       -webkit-box-orient: vertical;
     }
     .cmi_time{
       font-size:22rpx;
       color:#999999;
       text-align:right;
     }
   } 
 }
 
 .publishBox{
   position:fixed;
   left:0;
   bottom:0;
   right:0;
   padding:20rpx;
   background:#FFFFFF;
   color:#999999;
   .inputBox{
     padding:6rpx 10rpx;
     margin-right:20rpx;
     background:#F0F0F0;
     border-radius:8rpx;
   }
 }
 
 .release{
  display:flex;
  justify-content:flex-end;
 }
 
 .areaInput{
    box-sizing:border-box;
    width:100%;
    height:160rpx;
    background:#F0F0F0;
    padding:10rpx;
    margin-top:16rpx;
    font-size:26rpx;
    color:#999999;
 }
 
 .sendBtn{
   font-size:26rpx;
   background:#F0F0F0;
   width:120rpx;
   text-align:center;
   border-radius:30rpx;
   transition: all 1s linear;
 }
 
 .active{
   background:#B91B12;
   color:#FFFFFF;
   transition: background-color 1s linear,color 0.5s linear;
 }
</style>
