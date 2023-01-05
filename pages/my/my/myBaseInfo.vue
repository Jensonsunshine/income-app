<template>
	<view>
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>用户基础信息</text>
		</view>
		
		<view class="list" v-for="(list,list_i) in severList" :key="list_i">
			<view class="li" v-for="(li,li_i) in list" v-bind:class="{'noborder':li_i==list.length-1}"  hover-class="hover" :key="li.name" >
				<view class="text">{{li.name}}</view>
				<view class="text1" :style="'color:'+li.color+' ;'">{{li.content}}</view>
				<view v-if="li.name=='纳税人识别号'" style="width: 10% ;color: #007aff;">查看</view>
				<image class="to" :src="li.icon" v-else></image>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>户籍所在地</text>
		</view>
		<view class="list" v-for="(list1,list_i1) in severList1" :key="list_i1">
			<view class="li" v-for="(li1,li_i1) in list1" v-bind:class="{'noborder':li_i1==list1.length-1}"  hover-class="hover" :key="li1.name" >
				<view class="text">{{li1.name}}</view>
				<view class="text1" :style="'color:'+li1.color+' ;'">{{li1.content}}</view>
				<image class="to" :src="li1.icon"></image>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>经常居住地</text>
		</view>
		<view class="list" v-for="(list2,list_i2) in severList2" :key="list_i2">
			<view class="li" v-for="(li2,li_i2) in list2" v-bind:class="{'noborder':li_i2==list2.length-1}"  hover-class="hover" :key="li2.name" >
				<view class="text">{{li2.name}}</view>
				<view class="text1" :style="'color:'+li2.color+' ;'">{{li2.content}}</view>
				<image class="to" :src="li2.icon"></image>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>联系地址</text>
		</view>
		<view class="list" v-for="(list3,list_i3) in severList3" :key="list_i3">
			<view class="li" v-for="(li3,li_i3) in list3" v-bind:class="{'noborder':li_i3==list3.length-1}"  hover-class="hover" :key="li3.name" >
				<view class="text">{{li3.name}}</view>
				<view class="text1" :style="'color:'+li3.color+' ;'">{{li3.content}}</view>
				<image class="to" :src="li3.icon"></image>
			</view>
		</view>
		
		<view class="" style="width: 100%;height: 20upx;"></view>
		<view class="grid-title">
			<view></view>
			<text>其他</text>
		</view>
		<view class="list" v-for="(list4,list_i4) in severList4" :key="list_i4">
			<view class="li" v-for="(li4,li_i4) in list4" v-bind:class="{'noborder':li_i4==list4.length-1}"  hover-class="hover" :key="li4.name" >
				<view class="text">{{li4.name}}</view>
				<view class="text1" :style="'color:'+li4.color+' ;'">{{li4.content}}</view>
				<image class="to" :src="li4.icon"></image>
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
						{name:'姓名',content:'姚日天',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'证件类型',content:'居民身份证',color:'darkgray',icon:''},
						{name:'证件号码',content:'1****************1',color:'darkgray',icon:''},
						{name:'纳税人识别号',content:'1****************1',color:'black',icon:''},
						{name:'出生日期',content:'1990-01-01',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'性别',content:'男性',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'国籍(地区)',content:'中华人民共和国',color:'darkgray',icon:''},
					],
				],
				severList1:[
					[
						{name:'所在地区',content:'山西省蒲县',color:'black',icon:''},
						{name:'详细地址',content:'山西省蒲县克城镇公峪村251号',color:'black',icon:''},
					],
				],
				severList2:[
					[
						{name:'所在地区',content:'山西省蒲县',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'详细地址',content:'山西省蒲县克城镇公峪村251号',color:'black',icon:''},
					],
				],
				severList3:[
					[
						{name:'所在地区',content:'山西省蒲县',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'详细地址',content:'山西省蒲县克城镇公峪村251号',color:'black',icon:''},
					],
				],
				severList4:[
					[
						{name:'学历',content:'硕士',color:'black',icon:'../../../static/icons-income/my/to.png'},
						{name:'民族',content:'汉族',color:'darkgray',icon:'../../../static/icons-income/my/to.png'},
						{name:'电子邮箱',content:'15536790@163.com',color:'',icon:''},
					],
				],
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
.grid-title{
		display: flex;
		align-items: center;
		font-size: 32upx;
		color: rgba(0,0,0,.63);
		padding: 30upx 0;
		font-weight: 900;
		background-color: #FFFFFF;
		border-bottom: 1upx solid rgba(172,172,172,.2);
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
	
	.list{
		width:100%;border-bottom:solid 26upx #f1f1f1;background-color: white;
		.li{
			width:92%;height:85upx;padding:0 4%;border-bottom:solid 1upx #e7e7e7;display:flex;align-items:center;
		&.noborder{border-bottom:0}
			.text{width:33%;font-size: 32upx;}
			.text1{width:67%;font-size: 32upx;}
			.to{flex-shrink:0;width:40upx;height:40upx}
		}
	}
</style>
