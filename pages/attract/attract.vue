<template>
  <view class="content">
    <view class="imgBox">
      <image src="/static/images/2019cfsj_88.png"></image>
    </view>

    <view class="pathBox">
      <view class="pbTitle">加盟流程</view>
      <view class="stepBox uni-inline-item uni-flex-between">
        <view class="stepItem uni-column-item">
          <view class="stepImg">
            <image src="/static/images/2019cfsj_89.png" mode=""></image>
          </view>
          <view class="stepText">直接致电加盟服务热线</view>
        </view>
        <view class="stepItem uni-column-item">
          <view class="stepImg">
            <image src="/static/images/2019cfsj_90.png" mode=""></image>
          </view>
          <view class="stepText">电联做初步沟通</view>
        </view>
        <view class="stepItem uni-column-item">
          <view class="stepImg">
            <image src="/static/images/2019cfsj_91.png" mode=""></image>
          </view>
          <view class="stepText">见面与专家面谈细节</view>
        </view>
        <view class="stepItem uni-column-item">
          <view class="stepImg">
            <image src="/static/images/2019cfsj_92.png" mode=""></image>
          </view>
          <view class="stepText">正式签约盟合作</view>
        </view>
      </view>
    </view>

    <view class="main">
      <view class="introduce uni-inline-item">
        <view class="introImg">
          <image src="/static/images/2019cfsj_87.png"></image>
        </view>
        <view class="introWord">
          <view class="introTitle">
            为什么要加盟?
          </view>
          <view class="introText">
            走街串巷、报纸宣传、门口贴转让等方式已经落伍,互联网找店、转店信息平台是必然趋势,5年内,找店、
            转店互联网信息服务市场规模从必......
          </view>
        </view>
      </view>
      <view class="pbTitle">加盟条件</view>
      <view class="condition uni-inline-item">
        <view class="bedge">1</view>
        <text class="uni-flex-item uni-ellipsis">具有合法资格的法人或自然人。</text>
      </view>
      <view class="condition uni-inline-item">
        <view class="bedge">2</view>
        <text class="uni-flex-item uni-ellipsis">具有管理协调能力、有渠道经营经验。</text>
      </view>
      <view class="condition uni-inline-item">
        <view class="bedge">3</view>
        <text class="uni-flex-item uni-ellipsis">具有强烈的事业心、并有追求成功的欲望。</text>
      </view>
      <view class="condition uni-inline-item">
        <view class="bedge">4</view>
        <text class="uni-flex-item uni-ellipsis">具有一定的经济实力及长远的投资眼光。</text>
      </view>
      <view class="condition uni-inline-item">
        <view class="bedge">5</view>
        <text class="uni-flex-item uni-ellipsis">能正确看待和承担风险意识。</text>
      </view>
      <view class="condition uni-inline-item">
        <view class="bedge">6</view>
        <text class="uni-flex-item uni-ellipsis">想彻底改变命运的人。</text>
      </view>
      <view class="advantagebg">
        <image src="/static/images/2019cfsj_93.png"></image>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">大数据</view>
        <view class="adContent uni-flex-item">利用互联网大数据汇集海量找捕、转铺资源,采用智能匹配等方式一站式解决找铺、转铺难题</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">专业 专注 高效 </view>
        <view class="adContent uni-flex-item">7年专注找铺转铺这一件事，专业高效平均周期 20天到40天,成功率高达85% </view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">售后服务有保障</view>
        <view class="adContent uni-flex-item">全职专业的客服运营中心，网络运营中心，独创的流程控管服务系统等高端技术，全面保障售后</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">一站式整体服务提供商</view>
        <view class="adContent uni-flex-item">创新型的互联网＋商铺一站式整体解决方案提供商</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">市场大</view>
        <view class="adContent uni-flex-item"> 全国7000亿商铺市场，找铺转铺市场高达1000亿，前景广阔</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">免费加盟</view>
        <view class="adContent uni-flex-item"> 城市合作商迅猛扩张中，0加盟费，仅需少量运营管理费即可抢占城市合作商</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">总部全程支持</view>
        <view class="adContent uni-flex-item"> 团队打造扶持指导，物料支持，培训支持，推广支持，无需担心业务销售问题</view>
      </view>
      <view class="advantageItem uni-inline-item">
        <view class="adTitle">盈利模式</view>
        <view class="adContent uni-flex-item"> 一次加盟永久受益，二次分成，持续收益</view>
      </view>
    </view>

  </view>
</template>

<script>
  import uniBadge from "@/components/uni-badge/uni-badge.vue"
  export default {
    data() {
      return {

      };
    },
    components: {
      uniBadge
    }
  }
</script>

<style lang="scss" scoped>
  page,
  .content {
    width: 100%;
    height: 100%;
    background: #FAFAFA;
    overflow-y: scroll;
  }

  .imgBox {
    height: 250rpx;
    margin: 10rpx;
    border-radius: 10rpx;
    overflow: hidden;
  }

  .pbTitle {
    font-size: 36rpx;
    font-weight: 700;
    line-height: 44rpx;
    padding: 20rpx 0 20rpx 30rpx;
    position: relative;
    letter-spacing: 4rpx;
    color: #333;
    text-shadow: 0px -3px 4px #F59651, 0px -2px 3px #F59651, 0px -1.5px 2px #FB6229, 0px -1px 1.5px #FB6229, 0px -0.5px 1px #FB6229;

    &::after {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      margin: auto;
      width: 10rpx;
      height: 40rpx;
      // background: #FF0018;
      background: linear-gradient(45deg, yellow, blue, red);
      border-top-right-radius: 10rpx;
      border-bottom-right-radius: 10rpx;
    }
  }

  /*加盟流程样式*/
  .pathBox {
    padding: 20rpx;
    background: #FFFFFF;
    margin-bottom: 10rpx;

    .flowChart {
      margin: 10rpx 0;
      height: 200rpx;
      box-sizing: content-box;
      border-radius: 10rpx;
      overflow: hidden;
    }

    .stepBox {
      padding-bottom: 16rpx;
      overflow:hidden;
      .stepItem {
        box-sizing: border-box;
        width: 24%;
        height: 200rpx;
        padding: 20rpx;
        border-radius: 10rpx;

        &:nth-child(1) {
          background: #FFF4E0
        }

        &:nth-child(2) {
          background: #E0FBFF
        }

        &:nth-child(3) {
          background: #FFE0EA
        }

        &:nth-child(4) {
          background: #F1FFE0
        }

        .stepImg {
          width: 66rpx;
          height: 66rpx;
          margin-bottom:16rpx;
        }
        .stepText{
          color:#5C5C5C;
          font-size:24rpx;
          line-height:1.5;
          overflow: hidden;
          display: -webkit-box;
          text-overflow: ellipsis;
          -webkit-line-clamp:2;
          -webkit-box-orient:vertical;
        }
      }
    }
  }

  /*加盟流程样式*/

  /*加盟内容样式*/
  .main {
    padding: 0rpx 20rpx 20rpx;
    background: #FFFFFF;

    .introduce {
      padding: 20rpx 0;

      .introImg {
        width: 250rpx;
        height: 200rpx;
        flex-shrink: 0;
        border-radius: 10rpx;
        overflow: hidden;
      }

      .introWord {
        align-self: stretch;
        overflow: hidden;
        padding: 0 20rpx;

        .introTitle {
          font-size: 32rpx;
          line-height: 30rpx;
          font-weight: bold;
          padding: 16rpx 0;
        }

        .introText {
          font-size: 24rpx;
          line-height: 34rpx;
          color: #999999;
          overflow: hidden;
          display: -webkit-box;
          text-overflow: ellipsis;
          -webkit-line-clamp: 4;
          -webkit-box-orient: vertical;
        }
      }
    }

    .condition {
      padding: 0 20rpx;
      height: 60rpx;
      background: #FFFAFA;
      margin-top: 16rpx;
      border-radius: 10rpx;

      .bedge {
        width: 32rpx;
        height: 32rpx;
        line-height: 32rpx;
        font-size: 24rpx;
        margin-right: 20rpx;
        color: #FFFFFF;
        text-align: center;
        background: #FF6A6A;
        border-radius: 50%;
      }
    }

    .advantagebg {
      margin-top: 20rpx;
      height: 150rpx;
      border-radius: 10rpx;
      overflow: hidden;
    }

    .advantageItem {
      margin-top: 20rpx;
      height: 160rpx;
      overflow: hidden;

      &:nth-child(1n) {
        background: linear-gradient(to right, #FFF4E0, #FFFFFF);
      }

      &:nth-child(2n) {
        background: linear-gradient(to right, #E0F0FF, #FFFFFF);
      }

      &:nth-child(3n) {
        background: linear-gradient(to right, #FFEBFA, #FFFFFF);
      }

      .adTitle {
        padding: 0 20rpx;
        font-size: 32rpx;
        font-weight: bold;
        color: #6E6E81;
        width: 200rpx;
        text-align: center;
        line-height: 44rpx;
      }

      .adContent {
        font-weight: 400;
        color: #999999;
        line-height: 33rpx;
      }
    }
  }

  /*加盟内容样式*/
</style>
