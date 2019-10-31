<template>
	<view>
    <!--经纪人名片-->
		<view class="cardBox">
		  <view class="cardInfo uni-inline-item uni-flex-between">
		    <view class="uni-flex-item cardleft">
		      <view class="cardName">
		        <text>张晓明</text>
            <view class="certificate">
              <image src="/static/images/2019cfsj_11.png"></image>
            </view>
		      </view>
          <view class="">客户评价：100%</view>
          <view class="uni-ellipsis">主营商圈：东莞行政中心区数据的技术开发</view>
          <view class="uni-inline-item uni-flex-between">
            <view class="uni-inline-item cardBtn">
              <uni-icon type="phone-filled" color="#ffffff"></uni-icon>
              拨打电话
            </view>
            <view class="uni-inline-item cardBtn">
              <uni-icon type="chat" color="#ffffff"></uni-icon>
              立即沟通
            </view>
          </view>
		    </view>
        <view class="cardlogo">
          <image src="/static/images/2019cfsj_11.png" mode=""></image>
        </view>
		  </view>
		</view>
    <!--经纪人名片-->
     
    <!-- 客户评价-->
    <view class="correlationBox">
      <view class="uni-inline-item watchMore">
        <view class="wordStyle">客户评价</view>
        <view class="uni-inline-item wordStyle2">
          更多<uni-icon type="arrowright" color="#999999"></uni-icon>
        </view>
      </view>
      <view class="commentBox uni-inline-item">
        <view class="cm_left">
          <view class="uni-inline-item">
            房屋信息真实度：<uni-rate :size="28" :value="5" :is-fill="false" />
          </view>
          <view class="uni-inline-item">
            服务态度满意度：<uni-rate :size="28" :value="3" :is-fill="false" />
          </view>
          <view class="uni-inline-item">
            业务水平专业度：<uni-rate :size="28" :value="5"  :is-fill="false"/>
          </view>
        </view>
        <view class="cm_right uni-flex-item uni-column-item">
          <view class="grade">好评价：<text style="margin-left:0;color:#FF0018">100%</text></view>
          <button class="commentBtn">立即评价</button>
        </view>
      </view>
    </view>
    
    <!-- 客户评价-->
    
     <!--相关出租-->
    <view class="correlationBox">
      <view class="uni-inline-item watchMore">
        <view class="wordStyle">相关出租</view>
        <view class="uni-inline-item wordStyle2">
          更多<uni-icon type="arrowright" color="#999999"></uni-icon>
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
      </view>
    </view>
    <!--相关出租-->
	</view>
</template>

<script>
  import uniIcon from "@/components/uni-icon/uni-icon.vue";
  import uniRate from "@/components/uni-rate/uni-rate.vue";
	export default {
		data() {
			return {
				
			};
		},
    components:{
      uniIcon,
      uniRate
    }
	}
</script>

<style lang="scss" scoped>
 .cardBox{
   box-sizing:border-box;
   width:100%;
   height:423rpx;
   background-image: url('~@/static/images/2019cfsj_96.png');
   background-repeat:no-repeat;
   background-size:cover;
   padding:30rpx 20rpx;
   .cardInfo{
     box-sizing:border-box;
     background:#FFFFFF;
     width:100%;
     height:100%;
     padding:30rpx 20rpx;
     border-radius:10rpx;
     box-shadow:0rpx 0rpx 13rpx 0rpx rgba(0, 0, 0, 0.19);
   }
 }
 
 .cardleft{
   display:flex;
   flex-direction:column;
   justify-content:space-between;
   align-self:stretch;
   padding:20rpx;
   overflow: hidden;
 }
 
 .cardName{
   display:flex;
   align-items:flex-end;
   font-size:36rpx;
   font-weight:bold;
   line-height:1.5;
   .certificate{
     width:60rpx;
     height:35rpx;
     overflow:hidden;
   }
 }
 
 .cardlogo{
   width:250rpx;
   height:250rpx;
   border-radius:50%;
   overflow:hidden;
   flex-shrink:0;
 }
 
 .cardBtn{
   padding: 0 16rpx;
   border-radius:30rpx;
   color:#FFFFFF;
   &:nth-child(1){
    background:linear-gradient(90deg,rgba(255,108,71,1),rgba(252,61,78,1));
   }
   &:nth-child(2){
    background:linear-gradient(90deg,rgba(254,200,0,1),rgba(252,179,0,1));
   }
 }
 
 /*客户评价*/  
 .commentBox{
   padding:10rpx 20rpx 20rpx;
   .commentBtn{
     height:60rpx;
     line-height:60rpx;
     font-size:30rpx;
     background:#FFA901;
     color:#FFFDEF;
   }
   .grade{
     font-size:32rpx;
     font-weight:bold;
     margin-bottom:10rpx;
   }
 }
 /*客户评价*/
 
 
 /*相关出租*/
 .correlationBox{
   background:#FFFFFF;
   padding-bottom:20rpx;
   margin-bottom:10rpx;
   .watchMore{
     padding:10rpx 20rpx 0;
     justify-content:space-between;
   }
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
  /*相关出租*/
 
   /*列表框样式*/
    .listBox{
      padding:16rpx 10rpx 0;
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
    }
    
    .text2{
      font-weight:bold;
      margin-right:10rpx;
    }
    /*列表框样式*/
</style>
