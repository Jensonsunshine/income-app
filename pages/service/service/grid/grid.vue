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
	export default{
		name: 'zy-grid',
		props: {
			col: {	//每行显示格子数，支持每行3个或4个(默认为3)
				type: Number,
				value: 3
			},
			showTip: {	//格子菜单的数字角标(默认显示)
				type: Boolean,
				value: false
			},
			gridList: {
				type: Array,
				value: []
			},
			gridList2: {
				type: Array,
				value: []
			},
			gridList3: {
				type: Array,
				value: []
			},
			gridList4: {
				type: Array,
				value: []
			}
		},
		methods:{
			gridClick (item, index) {	//格子菜单点击事件
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
			border-radius: 40%;
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
