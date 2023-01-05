<template>
	<view>
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>请选择纳税记录年度</text>
		</view>
		<view class="grid">
			<view></view>
			<text class="text">年度</text>
			<picker @change="bindPickerChange" :value="index" :range="array" range-key="name" style="margin-right: 38%;">
				<view class="year">{{array[index].name}}</view>
			</picker>
			<image class="to" src="../../../static/icons-income/my/to.png"></image>
		</view>
		<view class="" style="width: 100%;height: 20upx;"></view>
		
		<view class="grid-title">
			<view></view>
			<text>请选择所得类型</text>
		</view>
		<view class="uni-list">
			<radio-group @change="radioChange">
				<label class="uni-list-cell uni-list-cell-pd" v-for="(item, index) in items" :key="item.value">
					<view>
						<radio :value="item.value" :checked="true" />
					</view>
					<view style="margin-left: 30upx;font-size: 32upx;">{{item.name}}</view>
				</label>
			</radio-group>
		</view>
		
		<view class="" style="width: 100%;height: 40upx;"></view>

		<view class="uni-padding-wrap uni-common-mt">
			<button type="primary" @click="selectIncome">查询</button>
		</view>	
	</view>
</template>

<script>
	export default {
	
		data() {
			return {
				array: [{
						name:'2019',
					},
					{
						name: '2020',
					}, 
					{
						name:'2021',
					}, 
					{
						name:'2022',
					}, 
					{
						name:'2023',
					},
				],
				index: 4,
				title: 'radio 单选框',
				items: [{
						value: '0',
						name: '工资薪金',
						checked: 'true'
					},
					{
						value: '1',
						name: '劳务报酬',
						checked: 'true'
					},
					{
						value: '2',
						name: '稿酬',
						checked: 'true'
					},
					{
						value: '3',
						name: '特许权使用费',
						checked: 'true'
					},
				],
				current: 0
			}
		},
		methods: {
			bindPickerChange: function(e) {
				console.log('picker发送选择改变，携带值为：' + e.detail.value)
				this.index = e.detail.value
			},
			
			radioChange(evt) {
				console.log(evt)
				for (let i = 0; i < this.items.length; i++) {
					if (this.items[i].value === evt.detail.value) {
						this.current = i;
						break;
					}
				}
			},
			selectIncome(e){
				uni.navigateTo({
					url:'./selectIncome?year=2023',
				})
			}
		}
	}
</script>

<style  lang="less" scoped>
	.uni-list-cell {
		justify-content: flex-start
	}
	
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
	.grid{
		display: flex;
		align-items: center;
		// flex-wrap: wrap;
		height:100upx;
		background-color: #FFFFFF;
		border-top: 2upx solid rgba(172,172,172,.2);
		// padding:0 4%;
		.text{
			padding-left:30upx;
			width:100%;
			color:#666;
			font-size: 35upx;
			height:100upx;
			line-height: 100upx;
			color: black;
		}
		.to{
			flex-shrink:0;
			width:40upx;
			height:40upx;
			line-height: 100upx;
			margin-right: 20upx;
		}
		.year{
			width:40upx;
			height:100upx;
			font-size: 35upx;
			line-height: 100upx;
			margin-right: 38%;
		}
	}
</style>
