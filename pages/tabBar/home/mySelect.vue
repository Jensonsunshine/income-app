<template>
	<view>
		<view class="" style="width: 100%;height: 20rpx;"></view>
		<view class="grid-title">
			<view></view>
			<text>申报信息查询</text>
		</view>
		
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20rpx">
				<label class="label" @click="toPage('./shen')" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">申报查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已申报的各项报表的查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
				
				<label class="label" @click="toPage('./zhuan')" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">专项附加信息扣除信息查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已填报的各项专项附加扣除记录的查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
	
				<label class="label" @click="toPage('../../service/service/IncomeDetails')" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">收入纳税明细查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已申报收入的查询及异议申诉</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
			</view>
		</view>
		
		
		<view class="" style="width: 100%;height: 20rpx;"></view>
		<view class="grid-title">
			<view></view>
			<text>备案信息查询</text>
		</view>
		
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20rpx">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">天使投资个人所得税抵扣备案查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已备案的创投企业和天使投资个人符合规定投资行为查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
				
				<label class="label" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">非货币性资产投资分期缴纳备案查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已备案的非货币性资产投资分期缴纳备案查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
			
				<label class="label" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">税收优惠备案查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已备案的税收优惠备案查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 20rpx;"></view>
		<view class="grid-title">
			<view></view>
			<text>其他查询</text>
		</view>
		
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20rpx">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">异议处理查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已发起的申诉事项的进度查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
				
				<label class="label" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">税务文书查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">税务机关送达的税务文书查询</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
			
				<label class="label" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">涉税专业服务机构查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">纳税人查询涉水专业服务机构信息</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
				
				<label class="label" style="height: 55upx;line-height: 55upx;border-top: 1rpx solid rgba(172,172,172,.2);;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;">纳税记录申请查询</text>
					<uni-icons type="forward" size="22" color="darkgray" style="margin-right: 30rpx;line-height: 55upx;float: right;"></uni-icons>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 28rpx;color: darkgray;float: left;">已申请开具的纳税记录</view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"></text>
				</label>
			</view>
		</view>
		
		
		<view class="" style="width: 100%;height: 600rpx;"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		methods: {
			toPage(url){
				console.log(url);
				uni.navigateTo({
					url:url
				})
			}
		}
	}
</script>

<style  lang="less" scoped>
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
			margin-right: 10upx;
			margin-left: 30upx;
			border-radius: 30upx;
		}
		text{
			color:black
		}
	}
	
	.to{
		// float: right;
		flex-shrink:0;
		width:30upx;
		height:30upx;
		line-height: 55upx;
		margin-right: 70upx;
		color:rgba(42, 90, 244, 1.0);
	}
	
</style>

