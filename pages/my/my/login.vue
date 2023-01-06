<template>
	<view>
		<view class="face" >
			<image :src="face" mode="" class="face-img"></image>
		</view>
		<view class="">
			<view class="form-item">
				<text class="form-type">账号</text>
				<input class="form-input"  placeholder="手机号码/证件号码" />
			</view>
			<view class="form-item">
				<text class="form-type">密码</text>
				<input class="form-input" placeholder="请输入密码" type="text" password />
			</view>
			<view class="form-item" style="border-bottom-style: none;">
				<text style="float: left;"></text>
				<text style="float: right;line-height: 100rpx;color: #007aff;">找回密码</text>
			</view>
			
			<view class="form-item" style="border-bottom-style: none;">
				<button type="primary">登陆</button>
			</view>
			
			<view class="form-item" style="border-bottom-style: none;">
				<button type="primary" plain="true">注册</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				face:'../../../static/icons-income/my/face.jpeg'
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
page{background-color:#fff}

	.face{
		width: 200rpx;
		height: 200rpx;
		margin: 100rpx  auto;
		border-radius: 50%;
		.face-img{
			width: 100%;
			height:100%;
			border-radius: 50%;
		}
	}
	.form-item{
		width:88%;
		height:100rpx;
		margin:0 auto;
		// padding:20rpx;
		border-bottom: 1rpx solid rgba(172,172,172,.2);
		.form-type{
			width:25%;
			float:left;
			line-height: 100rpx;
			// text-align: center;
			font-size: 32rpx;
		}
		.form-input{
			width:70%;
			height:100rpx;
			float:right;
			line-height: 100rpx;
			font-size: 32rpx;
			margin-left:1%;
			// text-align: center;
		}
	}
</style>
