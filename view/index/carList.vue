<template>
	<scroll-view scroll-x class="carList">
		<view class="scroll-wrapper">
			<view class="car-item" v-for='car in carlist' :key="car.carId">
				<div class='car-img-wrap'>
					<image class='car-img' :src="car.logo" mode="widthFix"></image>
				</div>
				<p class='car-name'>{{car.name}}</p>
				<p class='car-firstPay'>首付: {{car.firstPay}}万</p>
			</view>
		</view>
	</scroll-view>
</template>

<script>
	export default {
		data() {
			return {
				carlist: [{
					name: "雪佛兰",
					carId: 1,
					firstPay: '1.09',
					logo: 'http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png'
				},{
					name: "雪佛兰",
					carId: 2,
					firstPay: '1.09',
					logo: 'http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png'
				},{
					name: "雪佛兰",
					carId: 3,
					firstPay: '1.09',
					logo: 'http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png'
				},{
					name: "雪佛兰",
					carId: 4,
					firstPay: '1.09',
					logo: 'http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png'
				},{
					name: "雪佛兰",
					carId: 5,
					firstPay: '1.09',
					logo: 'http://pro1-img.huashenghaoche.com/cmall/2018/8/21/b2e24d854718495fb6c55c0f2321c8b4.png'
				}]
			}
		}
	}
</script>

<style lang="less">
	.carList {
		margin-top: 30upx;
		.scroll-wrapper {
			display:flex;
			align-items: flex-start;
			padding: 0 30upx;
			.car-item {
				border: 1px solid #fff;
				margin-right: 20upx;
				.car-img-wrap {
					width: 180px;
					text-align: center;
					background: #eee;
					border-radius: 14upx; 
					.car-img {
						width: 300upx;
					}
				}
				
				.car-name {
					color: #333;
					font-size: 26upx;
					line-height: 40upx;
				}
				.car-firstPay {
					color: #E83817;
					font-weight: 500;
					font-size: 26upx;
					line-height: 40upx;
				}
			}
			
		}
		
	}
</style>
