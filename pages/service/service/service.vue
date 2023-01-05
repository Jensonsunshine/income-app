<template>
	<view>
		<view class="grid-title">
			<view></view>
			<text>申报信息查询</text>
		</view>
		
		<view class="grid">
			<view :class="col == 3 ? 'grid-item-3' : 'grid-item-4'" v-for="(item, index) in gridList" :key="index" @click="gridClick(item, index)">
				<image :src="item.imgUrl" mode=""></image>
				<view v-text="item.name"></view>
				<text v-if="showTip && item.tips" v-text="item.tips"></text>
			</view>
		</view>
		
		<view style="height: 20upx;background-color: #f1f1f1;"></view>
		<view class="grid-title">
			<view></view>
			<text>备案信息查询</text>
		</view>
		<view class="grid">
			<view :class="col == 3 ? 'grid-item-3' : 'grid-item-4'" v-for="(item, index) in gridList2" :key="index" @click="gridClick(item, index)">
				<image :src="item.imgUrl" mode=""></image>
				<view v-text="item.name"></view>
				<!-- <text v-if="showTip && item.tips" v-text="item.tips"></text> -->
			</view>
		</view>
		
		<view style="height: 20upx;background-color: #f1f1f1;"></view>
		<view class="grid-title">
			<view></view>
			<text>其他查询</text>
		</view>
		<view class="grid">
			<view :class="col == 3 ? 'grid-item-3' : 'grid-item-4'" v-for="(item, index) in gridList3" :key="index" @click="gridClick(item, index)">
				<image :src="item.imgUrl" mode=""></image>
				<view v-text="item.name"></view>
				<text v-if="showTip && item.tips" v-text="item.tips"></text>
			</view>
		</view>
		
		<view style="height: 20upx;background-color: #f1f1f1;"></view>
		<view class="grid-title">
			<view></view>
			<text>公众服务</text>
		</view>
		<view class="grid">
			<view :class="col == 3 ? 'grid-item-3' : 'grid-item-4'" v-for="(item, index) in gridList4" :key="index" @click="gridClick(item, index)">
				<image :src="item.imgUrl" mode=""></image>
				<view v-text="item.name"></view>
				<text v-if="showTip && item.tips" v-text="item.tips"></text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data () {
			return {
				col:3,
				showTip:false,
				gridList:[	  //格子数据列表
					{
						name: '申报查询',
						imgUrl: '/static/icons-income/service/1.jpg',
						tips: ''
					},
					{
						name: '专项附加扣除信息查询',
						imgUrl: '/static/icons-income/service/2.jpg',
						tips: ''
					},
					{
						name: '收入纳税明细查询',
						imgUrl: '/static/icons-income/service/3.jpg',
						tips: '',
						url:'./IncomeDetails',
					},
				],
				gridList2:[	//备案
					{
						name: '天使投资个人所得税抵扣备案查询',
						imgUrl: '/static/icons-income/service/4.jpg',
						tips: ''
					},
					{
						name: '非货币性资产投资分期缴纳备案查询',
						imgUrl: '/static/icons-income/service/5.jpg',
						tips: ''
					},
					{
						name: '税收优惠备案查询',
						imgUrl: '/static/icons-income/service/6.jpg',
						tips: ''
					},
				],
				gridList3:[	//其他
					{
						name: '异议处理查询',
						imgUrl: '/static/icons-income/service/7.jpg',
						tips: ''
					},
					{
						name: '税务文书查询',
						imgUrl: '/static/icons-income/service/8.jpg',
						tips: ''
					},
					{
						name: '涉税专业服务机构查询',
						imgUrl: '/static/icons-income/service/9.jpg',
						tips: ''
					},
					{
						name: '纳税记录申请查询',
						imgUrl: '/static/icons-income/service/10.jpg',
						tips: ''
					},
				],
				gridList4:[	//公众
					{
						name: '票证查验',
						imgUrl: '/static/icons-income/service/16.jpg',
						tips: ''
					},
					{
						name: '通知公告',
						imgUrl: '/static/icons-income/service/12.jpg',
						tips: ''
					},
					{
						name: '税收政策及解读',
						imgUrl: '/static/icons-income/service/13.jpg',
						tips: ''
					},
					{
						name: '办税指南',
						imgUrl: '/static/icons-income/service/14.jpg',
						tips: ''
					},
					{
						name: '热点问题',
						imgUrl: '/static/icons-income/service/15.jpg',
						tips: ''
					},
				]
			}
		},
		props: {
			
		},
		methods:{
			gridClick (item, index) {	//格子菜单点击事件
				uni.navigateTo({
					url:item.url
				})
				console.log(item);
				console.log(index);
			}
		}
	}
</script>

<style lang="less" scoped>
	.grid-title{
		display: flex;
		align-items: center;
		font-size: 32upx;
		color: rgba(0,0,0,.63);
		padding: 30upx 0;
		font-weight: 900;
		background-color: #FFFFFF;
		view{
			width: 8upx;
			height: 30upx;
			background-color: rgba(42, 90, 244, 1.0);
			margin-right: 20upx;
			margin-left: 20upx;
			border-radius: 30upx;
		}
	}
	.grid{
		display: flex;
		align-items: center;
		flex-wrap: wrap;
		background-color: #FFFFFF;
		border-top: 2upx solid rgba(172,172,172,.2);
		.grid-item-3,.grid-item-4{
			box-sizing: border-box;
			width: calc(100% / 3);
			// border-bottom: 2upx solid rgba(172,172,172,.2);
			// border-right: 2upx solid rgba(172,172,172,.2);
			text-align: center;
			padding: 40upx 0;
			position: relative;
			image{
				width: 100upx;
				height: 100upx;
			}
			view{
				font-size: 28upx;
				margin-top: 16upx;
				color: rgba(0,0,0,.53);
			}
			text{
				display: block;
				padding: 4upx 8upx;
				text-align: center;
				border-radius: 36upx;
				font-size: 24upx;
				background-color: rgba(255,82,65,1);
				color: rgba(255,255,255,1);
				position: absolute;
				right: 6upx;
				top: 6upx;
			}
		}
		.grid-item-3:nth-child(3n + 3),.grid-item-4:nth-child(4n + 4){
			border-right: none;
		}
		.grid-item-4{
			width: calc(100% / 4);
		}
	}
</style>
