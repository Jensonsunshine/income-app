<template>
	<view>
		<view class="" style="width: 100%;height: 35upx;"></view>
		
		<view class="uni-list">
			<label class="uni-list-cell uni-list-cell-pd" v-for="(item, index) in items" :key="item.value">
				<view style="margin-left: 30upx;font-size: 32upx;">{{item.name}} 				
				<uni-icons type="help" color="#007aff" size="20"  v-show="item.value==0?true:false"/>
				:</view>
				<view style="font-size: 32upx;">{{item.total}}元</view>
			</label>
		</view>
		
		<view class="" v-for="(value, i) in lists" @click="goToInfo(value.id)">
			<view class="" style="width: 100%;height: 35upx;"></view>
			<view class="uni-list" style="padding:20upx 20upx 40upx 20upx;">
				<label class="label" style="height: 68upx;line-height: 68upx;">
					<text style="margin-left: 30upx;font-size: 35upx;float: left;">工资薪金</text>
					<text style="margin-right: 80upx;font-size: 35upx;float: right;">{{value.month}} </text>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 30upx;font-size: 30upx;color: darkgray;">所得项目小类：{{value.type}} </view>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 30upx;font-size: 30upx;color: darkgray;float: left;">扣缴义务人： {{value.agent}}</view>
					<image class="to" src="../../../static/icons-income/my/to.png"></image>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 30upx;font-size: 30upx;color: darkgray;">收入： {{value.income}}</view>
				</label>
				<label class="label"  style="height: 55upx;line-height: 55upx;">
					<view style="margin-left: 30upx;font-size: 30upx;color: darkgray;">已申报税额： {{value.declare}} </view>
				</label>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				items: [{
						value: '0',
						name: '收入合计',
						total:'453214.19'
					},
					{
						value: '1',
						name: '已申报税额合计',
						total:'12345.19'
					}
				],
				lists:[{
						id:0,
						month:'2022-12',
						type:'正常工资薪金',
						agent:'太原煤炭气化（集团）...',
						income:'13424.00元',
						declare:'193.48元'
					},
					{
						id:1,
						month:'2022-11',
						type:'正常工资薪金',
						agent:'太原煤炭气化（集团）...',
						income:'13424.00元',
						declare:'193.48元'
					},
					{
						id:2,
						month:'2022-10',
						type:'正常工资薪金',
						agent:'太原煤炭气化（集团）...',
						income:'13424.00元',
						declare:'193.48元'
					},
					{
						id:3,
						month:'2022-09',
						type:'正常工资薪金',
						agent:'太原煤炭气化（集团）...',
						income:'13424.00元',
						declare:'193.48元'
					}
				]
			}
		},
		onLoad(e) {
			console.log(e)  
			let obj = e.year.replace("\"([^\"]*)\"", "$1");  
			this.list = JSON.parse(obj)  
			console.log(this.list)
		},
		methods: {
			goToInfo(id){
				console.log(id)
				uni.navigateTo({
					url:'./selectIncomeInfo?id='+id,
				})
			}
		}
	}
</script>

<style>
	.to{
		float: right;
		flex-shrink:0;
		width:35upx;
		height:35upx;
		line-height: 55upx;
		margin-right: 70upx;
	}
</style>
