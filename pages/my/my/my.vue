<template>
	<view>
		<view class="header" v-bind:class="{'status':isH5Plus}">
			<view class="userinfo">
				<view class="face"><image :src="userinfo.face"></image></view>
				<view class="info" v-if="isLogin">
					<view class="username">{{userinfo.username}}</view>
					<view class="username">{{userinfo.mobile}}</view>
				</view>
				
				<view class="login" v-else @click="toLogin()">
					<view class="username">登陆/注册</view>
				</view>
			</view>
		</view>
		
		<view class="list" v-for="(list,list_i) in severList" :key="list_i">
			<view class="li" v-for="(li,li_i) in list" @click="toPage(li.url)" v-bind:class="{'noborder':li_i==list.length-1}"  hover-class="hover" :key="li.name" >
				<view class="icon"><image :src="'../../../static/icons-income/my/'+li.icon"></image></view>
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
				//#ifdef APP-PLUS
				isH5Plus:true,
				//#endif
				//#ifndef APP-PLUS
				isH5Plus:false,
				//#endif
				userinfo:{
					username:"姚日天",
					mobile:"188****8888",
					face:"../../../static/icons-income/my/face.jpeg"
				},
				isLogin:false,
				severList:[
					[
						{name:'个人信息',icon:'point.jpg',url:'./myInfo'},
						{name:'任职受雇信息',icon:'quan.jpg',url:'./employment'},
						{name:'家庭成员信息',icon:'momey.jpg'},
						{name:'银行卡',icon:'renw.jpg'},
						{name:'企业办税权限',icon:'renw1.jpg'},
					],
					[
						{name:'安全中心',icon:'anquan.jpg'},
					],
					[
						{name:'关怀版',icon:'mingxi.jpg'},
						{name:'帮助',icon:'choujiang.jpg'},
						{name:'我要咨询',icon:'addr.jpg'},
						{name:'关于',icon:'bank.jpg'},
						{name:'首页常用业务管理',icon:'security.jpg'},
					]
				],
			};
		},
		methods: {
			toPage(e){
				console.log(e)
				uni.navigateTo({
					url:e
				})
			},
			toLogin(){
				uni.navigateTo({
					url:'./login'
				})
			}
		}
	}
</script>


<style lang="scss">
page{background-color:#fff}
.header{
	&.status{padding-top:var(--status-bar-height);}
	background-color:#3e71e4;width:92%;height:30vw;padding:0 4%;display:flex;align-items:center;
	.userinfo{
		width:90%;display:flex;
		.face{flex-shrink:0;width:15vw;height:15vw;
			image{width:100%;height:100%;border-radius:100%}
		}
		.info{
			display:flex;flex-flow:wrap;padding-left:30upx;
			.username{width:100%;color:#fff;font-size:30upx}
			.integral{display:flex;align-items:center;padding:0 20upx;height:40upx;color:#fff;background-color:rgba(0,0,0,0.1);border-radius:20upx;font-size:24upx}
		}
		.login{
			display:flex;flex-flow:wrap;padding-left:30upx;margin-top: 30upx;
			.username{width:100%;color:#fff;font-size:40upx}
		}
	}
	.setting{
		flex-shrink:0;width:6vw;height:6vw;
		image{width:100%;height:100%}
	}
}
.hover{background-color:#eee}
.orders{
	background-color:#ff6364;width:92%;height:11vw;padding:0 4%;margin-bottom:calc(11vw + 40upx);display:flex;align-items:flex-start;border-radius:0 0 100% 100%;margin-top: -1upx;
	.box{
		width:98%;padding:0 1%;height:22vw;background-color:#fefefe;border-radius:24upx;box-shadow:0 0 20upx rgba(0,0,0,0.15);margin-bottom:40upx;display:flex;align-items:center;justify-content:center;
		.label{
			display:flex;align-items:center;justify-content:center;flex-flow:wrap;width:100%;height:16vw;color:#666666;font-size:26upx;
			.icon{
				position:relative;width:7vw;height:7vw;margin:0 1vw;
				.badge{position:absolute;width:4vw;height:4vw;background-color:#ec6d2c;top:-1vw;right:-1vw;border-radius:100%;font-size:20upx;color:#fff;display:flex;align-items:center;justify-content:center;z-index: 10;}
				image{width:7vw;height:7vw;z-index: 9;}
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
</style>
