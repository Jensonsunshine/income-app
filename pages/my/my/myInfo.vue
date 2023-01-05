<template>
	<view>
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="list" v-for="(list,list_i) in severList" :key="list_i">
			<view class="li" v-for="(li,li_i) in list" @click="toPage(li.url)" v-bind:class="{'noborder':li_i==list.length-1}"  hover-class="hover" :key="li.name" >
				<view class="text">{{li.name}}</view>
				<image class="to" src="../../../static/icons-income/my/to.png"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				severList:[
					[
						{name:'基本信息',icon:'point.jpg',url:'./myBaseInfo'},
						{name:'可享税收优惠',icon:'quan.jpg',url:'./employment'},
						{name:'其他身份证件',icon:'momey.jpg',url:''},
					],
				],
			}
		},
		methods: {
			toPage(e){
				console.log(e)
				uni.navigateTo({
					url:e
				})
			}
		}
	}
</script>

<style lang="scss">
	/* .to{
		float: right;
		flex-shrink:0;
		width:35upx;
		height:35upx;
		line-height: 55upx;
		margin-right: 70upx;
	} */
	
	.list{
		width:100%;border-bottom:solid 26upx #f1f1f1;background-color: white;
		.li{
			width:92%;height:100upx;padding:0 4%;border-bottom:solid 1upx #e7e7e7;display:flex;align-items:center;
		&.noborder{border-bottom:0}
			.icon{
				flex-shrink:0;width:50upx;height:50upx;
				image{width:50upx;height:50upx}
			}
			.text{padding-left:20upx;width:100%;font-size: 32upx;}
			.to{flex-shrink:0;width:40upx;height:40upx}
		}
	}
</style>
