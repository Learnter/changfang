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
        <view class="leftTitle">期望区域</view>
        <view class="rightInput uni-flex-item uni-flex">
           <xfl-select :list="list" :showItemNum="5" :placeholder = "'不限'" :selectHideType="'hideAll'"
           :style_Container="'padding:0;height:100%;border:none;'" style="flex:1"
           ></xfl-select>
        </view>          
      </view>
      
      <view class="uni-inline-item rowItem ">
        <view class="leftTitle">计划经营</view>
        <view class="rightInput uni-flex-item uni-flex">
         <xfl-select :list="list" :showItemNum="5" :placeholder = "'请选择计划经营行业'" :selectHideType="'hideAll'"
         :style_Container="'padding:0;height:100%;border:none;'" style="flex:1"
         ></xfl-select>
        </view>
      </view>
      
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">商铺类型</view>
        <view class="rightInput uni-flex-item uni-flex">
         <xfl-select :list="list" :showItemNum="5" :placeholder = "'档口/摊位/商铺'" :selectHideType="'hideAll'"
         :style_Container="'padding:0;height:100%;border:none;'" style="flex:1"
         ></xfl-select>
        </view>
      </view>
      
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">面积要求</view>
        <view class="rightInput uni-flex-item uni-flex">
         <xfl-select :list="list" :showItemNum="5" :placeholder = "'请选择可接受的面积范围(㎡)'" :selectHideType="'hideAll'"
         :style_Container="'padding:0;height:100%;border:none;flex:1'" style="flex:1"
         ></xfl-select>
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">租金预算</view>
        <view class="rightInput uni-flex-item uni-flex">
         <xfl-select :list="list" :showItemNum="5" :placeholder = "'请选择可接受的租金范围'" :selectHideType="'hideAll'"
         :style_Container="'padding:0;height:100%;border:none'" style="flex:1"
         ></xfl-select>
        </view>
      </view>
      
      <view class="uni-inline-item rowItem">
        <view class="leftTitle">是否接受转让费</view>
        <switch  @change="switchChange" style="transform:scale(0.8)" />
      </view>
      
      <view class="bottomBox">
        <button class="submit" type="warn">提交</button>
      </view>
    </view>
	</view>
</template>

<script>

  import xflSelect from '@/components/xfl-select/xfl-select.vue'; 
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
      xflSelect
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
      flex:1;
    }
  }
  
  /deep/.listHolder{
    font-size:28rpx;
    color:#BBBBBB;
  }
  
  .bottomBox{
   padding:50rpx 10rpx;
   letter-spacing:10rpx;
  }
  

</style>
