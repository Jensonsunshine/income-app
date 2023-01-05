<template>
	<view>
		<view class="" style="width: 100%;height: 25upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>纳税明细信息</text>
		</view>
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20upx 20upx 40upx 20upx;">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;color: darkgray;">收入：</text>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"> 3425.00 元</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">已申报税额： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"> 388.00 元</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="font-size: 30upx;color:rgba(42, 90, 244, 1.0);float: right;margin-right: 30upx;line-height: 55upx;">
						查看税款计算
						<uni-icons type="forward" size="22" color="#007aff" style="margin-right: 20upx;line-height: 55upx;"></uni-icons>
					</view>
				</label>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 25upx;"></view>
		
		<view class="grid-title">
			<view></view>
			<text>纳税明细-基础情况</text>
		</view>
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20upx 20upx 40upx 20upx;">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left:10upx;font-size: 30upx;float: left;color: darkgray;">所得项目小类：</text>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"> 正常工资薪金</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">扣缴义务人名称： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">太原煤炭气化（集团）有限责任公司</text>
				</label>
				
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">扣缴义务人纳税人识别号： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">91140500MA0LFX9F8C</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">主管税务机关： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">国家税务总局太原市税务局</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">申报渠道： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">办税大厅</text>
				</label>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 25upx;"></view>
		<view class="" >
			<view class="uni-list" style="padding:20upx 20upx 40upx 20upx;">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left: 10upx;font-size: 30upx;float: left;color: darkgray;">申报日期：</text>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">2022-12-15</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">税款所属期： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">2022-11</text>
				</label>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 25upx;"></view>
		<view style="background-color: #e5f2fe;padding: 20upx;">
			温馨提示：专项附加扣除和个人养老金已体现在税款计算过程
			中，在本期数据中不予显示。您可在“税款计算-累计收入与扣
			除详情”中查看。<text style="color:#007aff">查看税款计算</text>
		</view>
		<view class="grid-title">
			<view></view>
			<text>本期收入与扣除详情</text>
		</view>
		<view class="" style="border-top: 0.1upx solid rgba(172,172,172,.2);">
			<view class="uni-list" style="padding:20upx 20upx 40upx 20upx;">
				<label class="label" style="height: 55upx;line-height: 55upx;">
					<text style="margin-left:10upx;font-size: 30upx;float: left;color: darkgray;">本期收入：</text>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;"> 3452.00元</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">本期免税收入： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">0.00</text>
				</label>
				
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">本期减除费用： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">5000.00</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">本期专项扣除： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">0.00</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">本期其他扣除： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">0.00</text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 10upx;font-size: 30upx;color: darkgray;float: left;">本期准予扣除的捐赠项目： </view>
					<text style="margin-right: 50upx;font-size: 30upx;float: right;">0.00</text>
				</label>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				id:0
			}
		},
		onLoad(e) {
			console.log(e)  
			let obj = e.id.replace("\"([^\"]*)\"", "$1");  
			this.id = JSON.parse(obj)  
			console.log(this.id)
		},
		methods: {
			
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
