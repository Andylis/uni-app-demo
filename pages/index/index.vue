<template>
	<view class="content">
		<!-- 搜索 -->
		<view class="search-box">
			<input class="search-input" type="text" value="输入关键字搜索" />
		</view>
		<!-- 轮播图 -->
		<swiper class="index-swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" >
			<swiper-item v-for="image in swiperList" :key='image.id'>
				<view class="swiper-item">
					<image :src="image.src" class="swiper-img"></image>
				</view>
			</swiper-item>
		</swiper>
		<!-- 品牌列表 -->
		<view class="brand-list">
			<view class="brand-item" v-for="brand in brandList" :key='brand.id'>
				<image :src="brand.url" mode="" class="brand-img"></image>
				<text class="brand-name">{{brand.name}}</text>
			</view>
		</view>
		<!--  -->
		<bigWrap firstTitle='车好价优' secondTitle="低价格 高品质 居家出行首选"></bigWrap>
		<carList></carList>
	</view>
</template>

<script>
	import bigWrap from '../../view/index/big-wrap.vue';
	import carList from '../../view/index/carList.vue';
	export default {
		components:{
			bigWrap,
			carList
		},
		data() {
			return {
				title: 'Hello-uni-app',
				swiperList: [{
					id: 1,
					src: 'http://os01.huashenghaoche.com/cms/66102d17-cabe-4669-8ac7-eb4fd8df9d3e.jpg'
				},
				{
					id: 2,
					src: 'http://os01.huashenghaoche.com/cms/5eac669b-b16c-48ac-9ab1-93e6508db215.jpg'
				},
				{
					id: 3,
					src: 'http://os01.huashenghaoche.com/cms/da2cbe1e-8fc6-41ee-b521-b990a67cbe87.jpg'
				}],
				brandList:[{
					id: 1,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 2,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 3,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 4,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 5,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 6,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 7,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 8,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 9,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				},{
					id: 10,
					url: 'http://os01.huashenghaoche.com/cms/7f711409-5300-49d0-891f-44a518f1e73c.jpg',
					name: '奥迪'
				}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="less">
	.content { 
		width: 100%;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		.search-box {
			width: 80%;
			z-index: 2;
			position: absolute;
			top: 0;
			margin-top: 20upx;
			border-radius: 16px;
			text-align: center;
			background: rgba(231, 231, 231, 0.7);
			.search-input {
				font-size: 14px;
				color: #3d3d3d;
			}
		}
		
		.index-swiper {
			width: 100%;
			height: 360upx;
			.swiper-item {
				width: 100%;
				height: 360upx;
				.swiper-img {
					width: 100%;
					height: 360upx;
				}
			}
		}
		
		.brand-list{
			width: 100%;
			display: flex;
			justify-content: space-around;
			align-items: center;
			flex-wrap: wrap;
			margin-top: 20upx;
			.brand-item {
				display: flex;
				justify-content: center;
				align-items: center;
				flex-direction: column;
				width: 20%;
				padding: 15upx 0;
				// background: red;
				.brand-img {
					width: 60upx;
					height: 60upx;
				}
				.brand-name {
					margin-top: 5upx;
					color: #666;
					font-size: 24upx;
				}
			}
		}
	}
	
</style>
