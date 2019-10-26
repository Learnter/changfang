<template>
	<view>
		 <view class="logoBox uni-flex">
		    <view class="logo">
		      <image src="/static/images/2019cfsj_11.png"></image>
          <view class="albumBox" @tap="uploadImg">
            <image src="/static/images/2019cfsj_61.png"></image>
          </view>
		    </view>
		 </view>
     <view class="editBox">
       <view class="editItem uni-flex">
         <text>昵称</text>
         <view class="editText">
           <input type="text"  v-model="name" />
         </view>
       </view>
       <view class="editItem uni-flex">
         <text>性别</text>
         <view class="editText">
           <radio-group @change="chooseSex">
             <label class="radio">
               <radio value="boy" checked style="transform:scale(0.9)" />男
             </label>
             <label class="radio">
               <radio value="girl" style="transform:scale(0.9)"/>女
             </label>
           </radio-group>
         </view>
       </view>
       <view class="editItem uni-flex">
         <text>地区</text>
         <view class="editText">
          <picker mode="multiSelector" @columnchange="columnChange"  @change="onConfirm" :value="multiIndex" :range="multiArray">
            <input type="text"  placeholder-class="uni-ellipsis" :value="pickerText" disabled  />
          </picker>
         </view>
       </view>
       <view class="editItem uni-flex">
         <text>手机号码</text>
         <view class="editText">
           <input type="text" v-model="tel" />
         </view>
       </view>
       <view class="buttonBox">
         <button type="primary" class="confirm" @click="confirmSub">确定</button>
       </view>
     </view> 
	</view>
</template>

<script>
  import uniIcon from '@/components/uni-icon/uni-icon.vue'
	export default {
		data() {
			return {
				sex:'',
        multiArray: [],//联动地址列表
        multiIndex: [0, 0, 0],//显示地址
        pickerText:'',
        name:'科比布莱恩特',
        tel:'888888'
			};
		},
    methods:{
      /*选择性别*/
      chooseSex(e){
        this.sex = e.detail.value;
      },
      /*选择性别*/
      
      /*滚动列表改变*/
      columnChange(){
        
      },
      /*滚动列表改变*/
      
      /*确定地址选择*/
      onConfirm(){
        
      },
     /*确定地址选择*/ 
     
     /*确认提交*/
     confirmSub(){
       
     },
     /*确认提交*/
     
     /*更新上传头像*/
     uploadImg(){
       
     }
     /*更新上传头像*/
    },
    components:{
      uniIcon
    }
	}
</script>

<style lang="scss" scoped>
  .logoBox{
    padding:40rpx 20rpx;
    justify-content:center;
    position:relative;
    .logo{
      width:250rpx;
      height:250rpx;
      border-radius:50%;
      overflow:hidden;
      .albumBox{
        position:absolute;
        left:60%;
        top:60%;
        width:90rpx;
        height:90rpx;
        overflow:hidden;
      }
    }
  }
  
  .editBox{
    padding:0 20rpx;
    .editItem{
      padding:20rpx 0;
      border-bottom:1rpx solid #F4F4F4;
      font-size:36rpx;
      align-items:center;
    }
    .editText{
       flex:1;
       color:#999999;
       padding-left:50rpx;
       font-size:32rpx;
    }
    .buttonBox{
      margin-top:80rpx;
      .confirm{
        background:#B91B12;
        letter-spacing: 20rpx;
      }
    }
  }

</style>
