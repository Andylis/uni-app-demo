<template>
	<!-- <scroll-view class="floor-list" scroll-x>
		<view class="scoll-wrapper">
			<view 
				v-for="(item, index) in goodsList" :key="index"
				class="floor-item"
				@click="navToDetailPage(item)"
			>
				<image :src="item.image" mode="aspectFill"></image>
				<text class="title clamp">{{item.title}}</text>
				<text class="price">￥{{item.price}}</text>
			</view>
		</view>
	</scroll-view> -->
	
	<scroll-view scroll-x class="carList">
		<view class="scroll-wrapper">
			<view class="" v-for='car in carlist' :key="car.carId">
				<text>{{car.name}}</text>
				<image :src="car.logo" mode=""></image>
				
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
		.scroll-wrapper {
			display:flex;
			align-items: flex-start;
		}
		
	}
</style>
