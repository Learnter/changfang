<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import './common/uni.css';
  @import "./static/iconfont/iconfont.css";
	page {
		background: #FAFAFA;
    width:100%;
    height:100%;
		min-height:100%;
		/* font-size:28upx; */
		line-height:1.8;
		font-family: 'MicrosoftYaHei';
	}
	
	.fx1 {
		-webkit-flex: 1;
		flex: 1;
	}
	
	.clearfix::after {
		content: "";
		display: block;
		clear: both;
	}
	
	*{
		box-sizing: content-box;
		box-sizing: border-box;
	}
  
  image{
    width:100%;
    height:100%;
    will-change: transform
  }
    
</style>
