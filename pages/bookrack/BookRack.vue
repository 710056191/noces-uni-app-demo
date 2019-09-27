<template>
	<view>
		<view class="current">
			<view class="current-img">
				<image src="../../static/logo.png" mode="widthFix"></image>
			</view>
			<view class="current-text">
				<h3>思维的力量</h3>
				<text>(美)道格拉斯.勒登</text>
				<text>当前进度：{{current_text}}</text>
				<button type="primary" size="mini">继续阅读</button>
			</view>
		</view>
		<view class="list">
			<view class="list-text" v-for="(item,index) in racklist" :key='index'>
				<uniTag type="default" :text="item.tag" size="small"></uniTag>
				<image :src="item.src" mode="widthFix"></image>
				<h3>{{item.title}}</h3>
				<text>{{item.plan}}</text>
			</view>
		</view>
	</view>
</template>

<script>
	
	import uniTag from "@/components/uni-tag/uni-tag.vue"
	export default{
		name:'BookRack',
		components:{uniTag},
		data(){
			return {
				title:'bookrack',
				current_text:'第一章 争取是生存的关键',
				racklist:[{
					src:'../../static/logo.png',
					title:'蜜汁炖鱿鱼',
					plan:'已读100%',
					tag:'读完'
				}]
			}
		}
	}
</script>

<style lang="scss">
	.current{
		display: flex;
		background: #F5F5F7;
		padding: 10px 20px 25px 15px;
		.current-img{
			width: 35%;
			margin-right: 10px;
			uni-image{
				width: 100%;
			}
		}
		.current-text{
			width: 60%;
			margin: auto 0;
			h3{
				font-size: 18px;
			}
			uni-text{
				font-size: 14px;
				color: #A1A5B3;
			}
			uni-button{
				border-radius:36px;
			}
		}
	}
	.list{
		padding-top: 10px;
		.list-text{
			width: 30%;
			display: inline-block;
			padding: 0 0 3% 3%;
			box-sizing: border-box;
			uni-image{
				width: 90%;
			}
			h3{
				font-size: 16px;
			}
			uni-text{
				font-size: 12px;
				color:#999999;
			}
		}
	}
</style>
