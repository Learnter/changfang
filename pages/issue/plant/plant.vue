<template>
	<view class="content">
    <view class="list">
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">标题</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入标题" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem ">
        <view class="leftTitle">姓名</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入姓名" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">联系电话</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value="" placeholder="请输入您的联系方式" placeholder-class="listHolder"/>
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">当前经营</view>
        <view class="rightInput uni-flex-item uni-flex">
           <xfl-select :list="list" :showItemNum="5" :placeholder = "'请选择当前经营的行业'" :selectHideType="'hideAll'"
           :style_Container="'padding:0;height:100%;border:none;'" style="flex:1"
           ></xfl-select>
        </view>          
      </view>
      
      <view class="uni-inline-item rowItem ">
        <view class="leftTitle">当前区域</view>
        <view class="rightInput uni-flex-item uni-flex">
         <xfl-select :list="list" :showItemNum="5" :placeholder = "'您铺位所在区域'" :selectHideType="'hideAll'"
         :style_Container="'padding:0;height:100%;border:none;'" style="flex:1"
         ></xfl-select>
        </view>
      </view>
      
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">详细地址</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入详细地址" placeholder-class="listHolder" />
        </view>
      </view>
      
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">店铺面积</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入您商铺的使用面积(㎡)" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">月租金</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入您商铺的月租金(元/月)" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">剩余租期</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入店铺最长租期 例:12个月" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">转让费用</view>
        <view class="rightInput uni-flex-item uni-flex">
          <input type="text" value=""  placeholder="请输入您的转让费(万元)" placeholder-class="listHolder" />
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle" style="color:#B91B12;font-weight:400">添加地图定位</view>
        <uni-icon type="location-filled" color="#B91B12" size="25"></uni-icon>
      </view>
     
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">是否展示为面议</view>
        <switch  @change="switchChange" style="transform:scale(0.8)" />
      </view>
      
      <view class="uni-flex storeImgs">
        <view class="leftTitle">店铺照片</view>
        <view class="uni-flex-item">
         <view class="upNotice">(提示：请至少上传一张正面照，图片越多可提高转出速度)</view>
         <view class="uni-flex imgBox">
           <view class="uni-column-item unloadImg">
             <view class="uploadButton">
                <image src=""></image>
             </view>
             <view>正面照</view>
           </view>
           
        <!--  <view class="uploadButton" style="margin-right:20rpx" v-for="(item,index) in 4" :key='index'>
             <image src="/static/images/jiatu.png" mode=""></image>
           </view> -->
           
           <view class="uni-column-item unloadImg">
             <view class="uploadButton"></view>
             <view>上传更多</view>
           </view>
         </view>
        </view>
      </view>
      
      <view class="bottomBox">
        <button class="submit" type="warn">发布</button>
      </view>
    </view>
	</view>
</template>

<script>
  import xflSelect from '@/components/xfl-select/xfl-select.vue'; 
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
	export default {
		data() {
			return {
				list:[]
			};
		},
    methods:{
      switchChange(){
        
      }
    },
    components:{
      xflSelect,
      uniIcon
    }
	}
</script>

<style lang="scss" scoped>
  .content{
    box-sizing:border-box;
    width:100%;
    height:100%;
    padding:20rpx 20rpx 40rpx;
    overflow-y: scroll;
  }
  
  .list{
    background:#FFFFFF;
    border-radius:20rpx;
    box-shadow: 0 16rpx 16rpx rgba(10, 16, 20, .24), 0 0 16px rgba(10, 16, 20, .12);
  }
  
  .rowItem{
    height:80rpx;
    margin-bottom:20rpx;
    justify-content:space-between;
  }
  
  .leftTitle{
    font-size:32rpx;
    font-weight:bold;
    min-width:160rpx;
    margin: 0 20rpx 0 10rpx;
    letter-spacing:6rpx;
  }
  
  .rightInput{
    align-self:stretch;
    align-items:flex-end;
    padding:10rpx 16rpx;
    border-bottom:2rpx solid #D9D9D9;
    input{
      flex:1
    }
  }
  
 /deep/.listHolder{
    font-size:28rpx;
    color:#BBBBBB;
  }
  
  .bottomBox{
   padding:50rpx 10rpx;
  }
  
  .upNotice{
    font-size:22rpx;
    color:#ADADAD;
    line-height:32rpx;
    letter-spacing:1rpx;
  }
  
  .uploadButton{
    width:130rpx;
    height:130rpx;
    margin-bottom:6rpx;
    background-image:url(~@/static/images/jiatu.png);
    background-repeat: no-repeat;
    background-size: cover;
  }
  
  .imgBox{
    margin:20rpx 0;
    flex-wrap:wrap;
    .unloadImg{
      margin-right:20rpx;
      font-size:28rpx;
      color:#999999;
    }
  }
 
</style>