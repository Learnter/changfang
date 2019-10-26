<template>
	<view>
		<view class="jzhometopBoxHe">
			<view class="jzhometopBox">
				<swiper :indicator-dots="true" indicator-color="rgba(255,255,255,0.7)" current="0" 
				indicator-active-color="#4395FC" :autoplay="true" :interval="3000" :duration="1000" circular="true" style="height: 350rpx;">
					<swiper-item class="bannImg">
						<view class="swiper-item">
							<image src="../../static/images/2019cfsj_1.png" mode="aspectFill" class="bannImg"></image>
						</view>
					</swiper-item>
					<swiper-item class="bannImg">
						<view class="swiper-item">
							<image src="../../static/images/2019cfsj_1.png" mode="aspectFill" class="bannImg"></image>
						</view>
					</swiper-item>
					<swiper-item class="bannImg">
						<view class="swiper-item">
							<image src="../../static/images/2019cfsj_1.png" mode="aspectFill" class="bannImg"></image>
						</view>
					</swiper-item>
				</swiper>
			</view>
			<view class="jzhometinputBox">
				<view class="uni-flex jzhometinpHe">
					<view class="jzhomedzhi">东莞市</view>
					<view class="jzhomezxan"><uni-icon type="arrowdown" color="#eeeeee" size="12"/></view>
					<view class="fx1">
						<navigator url="#" hover-class="none">
							<view class="uni-flex jzhomessBox">
								<view class="jzhomessimg">
									<image src="../../static/images/2019cfsj_2.png" mode="aspectFit"></image>
								</view>
								<view class="fx1 jzhomesstx">搜索你想要的店铺或区域</view>
							</view>
						</navigator>
					</view>
				</view>
			</view>
		</view>
		
		<view class="clearfix jzhomNavBoxHe">
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_40.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">厂房</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_41.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">仓库</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_42.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">产业园</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_40.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">小面积</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_41.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">委托找房</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_42.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">待办环评</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_40.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">厂房装修</view>
			</navigator>
			<navigator url="" hover-class="none" class="jzhomNavBox">
				<view class="jzhomNavimg">
					<image src="../../static/images/2019cfsj_41.png" mode=""></image>
				</view>
				<view class="jzhomNavtx">企业服务</view>
			</navigator>
		</view>
		
		<view class="jzhotleBox uni-flex">
			<view class="jzhotlehx"></view>
			<view class="jzhotletxx fx1">热门出租</view>
		</view>
		<view class="jzscrmczListHe">
			<scroll-view scroll-x="true" >
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>
				<navigator url="#" hover-class="none" class="jzscrmczList">
					<image src="../../static/images/2019cfsj_4.png" mode=""></image>
					<view class="jzscrmczTx">CBD/国贸</view>
				</navigator>				
			</scroll-view>
		</view>
		<view class="uni-swiper-msg jzgdggBox">
			<view class="uni-swiper-msg-icon">
				<image src="../../static/images/2019cfsj_44.png" mode="widthFix"></image>
			</view>
			<swiper autoplay="true" circular="true" interval="5000">
				<swiper-item v-for="(item, index) in msg" :key="index">
					<navigator>{{item}}</navigator>
				</swiper-item>
			</swiper>
		</view>
		
		<view class="jzhoertleBox uni-flex">
			<view class="jzhotlehx"></view>
			<view class="jzhotletxx fx1">厂房出租</view>
			<view class="jzhotletggui">换一批&gt;</view>
		</view>
		<view class="jzhochptBox clearfix">
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门镇</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门镇</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门镇</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门镇</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
		</view>
		
		
		<view class="jzhoertleBox uni-flex">
			<view class="jzhotlejjr fx1">经纪人</view>
			<navigator url="#" class="jzhotletggui" hover-class="none">更多&gt;</navigator>			
		</view>
		<view class="jzscrmczListHe">
			<scroll-view scroll-x="true">
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
				<navigator url="#" class="jinjrBox" hover-class="none">				
					<view class="jinjrimg">
						<image src="../../static/images/2019cfsj_11.png" mode=""></image>
					</view>
					<view class="jinjrtxt">吉吉王</view>				
				</navigator>
			</scroll-view>
		</view>
		
		
		<view class="jzhoertleBox uni-flex">
			<view class="jzhotlehx"></view>
			<view class="jzhotletxx fx1">土地出租</view>
			<navigator url="#" class="jzhotletggui" hover-class="none">更多&gt;</navigator>	
		</view>
		<view class="jzhochptBox clearfix">
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">高埗</view>
						<view class="jzhochptmshu">高淳开发区，工业地皮出售，先进.....</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市高埗高淳开发区</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">南城</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市高埗高淳开发区</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">高埗</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">南城</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
		</view>
		
		
		<view class="jzhoertleBox uni-flex">
			<view class="jzhotlehx"></view>
			<view class="jzhotletxx fx1">写字楼出租</view>
			<navigator url="#" class="jzhotletggui" hover-class="none">更多&gt;</navigator>	
		</view>
		<view class="jzhochptBox clearfix">
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门万达广场</view>
						<view class="jzhochptmshu">高淳开发区，工业地皮出售，先进......</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市高埗高淳开发区</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">经贸广场</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市高埗高淳开发区</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">虎门万达广场</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
			<navigator url="#" hover-class="none" class="jzhochptlist">				
				<view class="jzhochptlihe">
					<view class="jzhochptliziz">
						<view class="jzhochptmic">经贸广场</view>
						<view class="jzhochptmshu">东莞市虎门镇科技园十六栋b楼</view>
						<view class="jzhochptimg">
							<image src="../../static/images/2019cfsj_6.png" mode=""></image>
						</view>
						<view class="jzhochpdizhihe">
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_43.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">东莞市虎门镇科技园十六栋b楼</view>
							</view>
							<view class="jzhochpdizhi uni-flex">
								<image src="../../static/images/2019cfsj_19.png" mode=""></image>
								<view class="fx1 jzhochpdizhitx">18200003333</view>
							</view>
						</view>					
					</view>
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
  import uniIcon from '@/components/uni-icon/uni-icon.vue'
	export default {
		data() {
			return {
				msg : [
					'今日十点二十分，美国总统奥巴马摆放拜访中国总理，希望中美......',
					'DCloud完成B2轮融资，uni-app震撼发布',
					'36氪热文榜推荐、CSDN公号推荐 DCloud CEO文章'
				]
			}
		},
		onLoad() {

		},
		methods: {

		},
    components:{
      uniIcon
    }
	}
</script>

<style>
	@import url("index.css");
</style>
1