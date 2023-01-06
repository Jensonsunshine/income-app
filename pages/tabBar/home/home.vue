<template>
	<view>
		<view class="header">
			<view class="uni-margin-wrap">
				<swiper class="swiper" circular :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
					<swiper-item>
						<view class="swiper-item" style="background-image:url('../../../static/icons-income/home/banner1.png');height:100%;width:100%;overflow: hidden;background-size:cover;">
						</view>
					</swiper-item>
					<swiper-item>
						<view class="swiper-item" style="background-image:url('../../../static/icons-income/home/banner2.png');height:100%;width:100%;overflow: hidden;background-size:cover;">
	
						</view>
					</swiper-item>
					<swiper-item>
						<view class="swiper-item" style="background-image:url('../../../static/icons-income/home/banner3.png');height:100%;width:100%;overflow: hidden;background-size:cover;">
						</view>
					</swiper-item>
					<swiper-item>
						<view class="swiper-item" style="background-image:url('../../../static/icons-income/home/banner4.png');height:100%;width:100%;overflow: hidden;background-size:cover;">
						</view>
					</swiper-item>
				</swiper>
			</view>
		</view>
		<view class="orders">
			<view class="box">
				<view class="label" v-for="(row,index) in orderTypeLise" :key="row.name" hover-class="hover" @click="goToPage(row.url,row.type)">
					<view class="icon"><image :src="'../../../static/icons-income/'+row.icon"></image></view>
					{{row.name}}
				</view>
			</view>
		</view> 
		
		<view class="img-body">
			<view class="img-home-body" >
				<image class="body-img" src="/static/icons-income/home/210.jpeg" mode=""></image>
			</view>
			
			<view class="img-home-body" @click="goToPage('../../service/service/IncomeDetails',2)">
				<image class="body-img-1" src="/static/icons-income/home/211.jpeg" mode=""></image>
			</view>
			
			<view class="img-home-body">
				<image class="body-img-2" src="/static/icons-income/home/212.jpeg" mode=""></image>
			</view>
		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				orderTypeLise:[
					{name:'我要办税',icon:'1.png',url:'/pages/do/do',type:1},
					{name:'我要查询',icon:'2.png',url:'/pages/tabBar/home/mySelect',type:2},
					{name:'公众服务',icon:'3.png',url:'/pages/service/service/service',type:1},
				],
				background: ['color1', 'color2', 'color3'],
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500
			}
		},
		onLoad() {
		
		},
		methods: {
			changeIndicatorDots(e) {
				this.indicatorDots = !this.indicatorDots
			},
			changeAutoplay(e) {
				this.autoplay = !this.autoplay
			},
			intervalChange(e) {
				this.interval = e.detail.value
			},
			durationChange(e) {
				this.duration = e.detail.value
			},
			goToPage(e,type) {
				console.log("跳转页面："+e)
				if(type == 1){
					uni.switchTab({
						url:e
					})	
				}else{
					uni.navigateTo({
						url:e
					})
				}
				
			}
		}
	}
</script>

<style lang="scss">
page{background-color:#fff}
	.header{
		width:100%;height:550rpx;margin:0 auto;display:flex;align-items:center;border-radius:0 0 5% 5%;background-size: cover;overflow: hidden;
	}
	// .hover{background-color:#eee}
	.orders{
		width:92%;height:11vw;padding:0 4%;margin-bottom:calc(11vw + 40upx);display:flex;align-items:flex-start;
		margin-top: -75upx;
		.box{
			width:98%;padding:0 10%;height:25vw;background-color:#fefefe;border-radius:15upx;box-shadow:0 0 20upx rgba(0,0,0,0.15);margin-bottom:40upx;display:flex;align-items:center;justify-content:center;z-index: 100;
			.label{
				display:flex;align-items:center;justify-content:center;flex-flow:wrap;width:100%;height:18vw; color:#666666;font-size:26upx;
				.icon{
					position:relative;width:15vw;height:15vw;margin:0 3vw;
					image{width:15vw;height:15vw;z-index: 109;}
				}
			}
		}
	}

	.list{
		width:100%;border-bottom:solid 26upx #f1f1f1;
		.li{
			width:92%;height:100upx;padding:0 4%;border-bottom:solid 1upx #e7e7e7;display:flex;align-items:center;
		&.noborder{border-bottom:0}
			.icon{
				flex-shrink:0;width:50upx;height:50upx;
				image{width:50upx;height:50upx}
			}
			.text{padding-left:20upx;width:100%;color:#666}
			.to{flex-shrink:0;width:40upx;height:40upx}
		}
	}


	.uni-margin-wrap {
		height:550rpx;
		width: 100%;
		border-radius:0 0 5% 5%;
		overfloat:hidden;
		
	}
	.swiper {
		height:550rpx;
		border-radius:0 0 5% 5%;
		overfloat:hidden;
	}
	
	.swiper-item {
		// display: block;
		height: 100%;
		line-height: 100%;
		text-align: center;
		border-radius:0 0 5% 5%;
		overfloat:hidden;
	}	
	
	.img-body{
		width: 100%;
		text-align: center;
		height: 100%
	}
	
	.img-home-body{
		width: 100%;
		height: 100%;
	}
	
	.body-img{
		width: 100%;
		height:1000upx ;
	}
	
	.body-img-1{
		width: 100%;
		height:210rpx ;
	}
	
	.body-img-2{
		width: 100%;
		height:1200rpx ;
	}
	
	.footer-img{
		width: 100%;
		height: 1000upx;
	}
</style>