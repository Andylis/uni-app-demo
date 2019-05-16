<template>
	<view class="big-wrap">
		<view class="text">
			<p class='first-title'>{{firstTitle}}<p>
			<p class='second-title'>{{secondTitle}}</p>
			<p class='check-more'>查看更多</p>
		</view>
		<image class="car-img" src="http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png" mode="widthFix"></image>
	</view>
	
</template>

<script>
	export default {
		props: {
			firstTitle: {
				type: String,
				default: () => {}
			},
			secondTitle: {
				type: String,
				default: () => {}
			}
		}
	}
	
</script>

<style lang="less">
	.big-wrap {
		display: flex;
		flex-direction: row;
		align-items: center;
		width: 90%;
		box-sizing: border-box;
		height: 240upx;
		padding: 10upx 0upx 10upx 30upx;
		margin-top: 30upx;
		background: cadetblue;
		border-radius: 10upx;
		.text {
			width: 550upx;
			.first-title {
				color: #fff;
				font-size: 40upx;
			}
			.second-title {
				color: rgba(255, 255, 255, .8);
				font-size: 24upx;
			}
			.check-more {
				margin-top: 20upx;
				width: 100upx;
				padding: 8upx 20upx;
				text-align: center;
				font-size: 20upx;
				color: #fff;
				border: 1px solid rgba(255, 255, 255, .8);
				border-radius: 2px;
			}
		}
		.car-img {
			float: right;
			width:500upx;
		}
	}
</style>
