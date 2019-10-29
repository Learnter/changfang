<template>
	<view class="content">
		<view class="uni-inline-item typeBox">
		  <text>投诉类型</text>
      <view class="selType uni-flex-item">-----请选择<uni-icon :type=typeIcon   size="22" color="#949494"></uni-icon>-----</view> 
		</view>
    <view class="listBox uni-inline-item">
      <view class="listItem" v-for="(item,index) in 5" :key="index">客服不回复</view>
    </view>
    <textarea maxlength=-1  value="" placeholder="请输入内容......" class="areaBox"  placeholder-class="areaHolder"/>
    <view class="uploadBox">
      <view class="uni-inline-item">
        <text class="uploadTitle">添加截图</text>
        <view class="example">(例如:客服不会消息的页面截图)</view>
      </view>
      <view class="uploadImgs uni-flex">
        <view class="uploadButton" v-for="(item,index) in imgs" :key="index">
          <image :src="item"></image>
        </view>
        <view class="uploadButton" @click="uploadFile">
          <image src="/static/images/jiatu.png" ></image>
        </view>
      </view>
    </view>
    <button type="warn" class="submit">提交</button>
    
    <!--提交成功弹框提示-->
    <uni-popup ref="popup" type="center">
      <view class="smileImg">
        <image src="/static/images/2019cfsj_94.png" mode=""></image>
      </view>
      <view class="popBox">
        <view class="popTips">
          提交成功，我们将第一时间 处理您提交你的信息 
        </view>
        <view class="confirmBtn" @click="$refs['popup'].close()">
          知道了
        </view>
      </view>
    </uni-popup>
	</view>
</template>

<script>
  import uniIcon from '@/components/uni-icon/uni-icon.vue';
  import uniPopup from '@/components/uni-popup/uni-popup.vue';
	export default {
		data() {
			return {
				typeIcon:'arrowdown',
        imgs:[]
			};
		},
    onReady() {
      this.$refs['popup'].open();
    },
    methods:{
      uploadFile(){
        uni.chooseImage({
            count: 3, //默认9
            sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
            sourceType: ['album'], //从相册选择
            success: (res)=> {
                this.imgs = res.tempFilePaths;
            }
        });
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
  }
  .content{
    padding:20rpx 20rpx 0;
    box-sizing:border-box;
  }
  
  .areaHolder{
    color:#949494;
    font-size:26rpx;
  }
  
  .typeBox{
    color:#333333;
    margin-bottom:20rpx;
    .selType{
      background:#F5F5F5;
      text-align:center;
      border-radius:10rpx;
      color:#949494;
      padding:10rpx 0;
    }
  }
  
  .areaBox{
    box-sizing:border-box;
    width:100%;
    height:240rpx;
    padding:16rpx;
    box-shadow:0rpx 1rpx 7rpx 0rpx rgba(0, 0, 0, 0.15);
    font-size:28rpx;
    line-height:36rpx;
    margin-bottom:20rpx;
    border-radius:8rpx;
    overflow: hidden;
  }
  
  .listBox{
    flex-wrap:wrap;
    .listItem{
      padding:6rpx 25rpx;
      border-radius:20rpx;
      background:#F0F0F0;
      margin:0 20rpx 20rpx 0;
      font-size:26rpx;
      color:#616161;
    }
  }
  
  .uploadTitle{
   font-size:30rpx;
   font-weight:600;
   color:#333333;
  }
  
  .example{
    font-size:24rpx;
    color:#999999;
  }
  
  .uploadImgs{
    overflow:hidden;
    flex-wrap:wrap;
  }
  
  .uploadButton{
    width:130rpx;
    height:130rpx;
    margin-top:20rpx;
    margin-right:20rpx;
  }
  
  .submit{
    margin:100rpx 0;
  }
  
  
  /*成功弹框样式*/
  .popBox{
   width:456rpx;
   height:300rpx;
   overflow:hidden;
   position:relative;
     .popTips{
       position:absolute;
       top:80rpx;
       line-height:1.5;
     }
     .confirmBtn{
       position:absolute;
       bottom:0;
       left:50%;
       transform: translateX(-50%);
       width:240rpx;
       height:60rpx;
       line-height:60rpx;
       color:#FC3D4E;
       border:2rpx dashed #FC3D4E;
       border-radius:30rpx;
       font-size:30rpx;
     }
  }
  
  /deep/.uni-popup__wrapper-box {
    border-radius:20rpx;
  }
  
  /deep/.uni-popup__wrapper.uni-custom.center .uni-popup__wrapper-box {
  	overflow-y: inherit;
    box-shadow: 0 0 10rpx #FFFACD;
  }
  
  .smileImg{
    position:absolute;
    top:-75rpx;
    left:50%;
    transform: translateX(-50%);
    width:150rpx;
    height:150rpx;
    border-radius:50%;
    overflow:hidden;
    
  }
  /*成功弹框样式*/
</style>
