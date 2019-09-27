<template>
	<view class="book-list-content">
		<view class="list" v-for="(item,index) in list" :key='index'>
			<image :src="item.src" mode="widthFix"></image>
			<h4>{{item.title}}</h4>
			<text>
				<span>{{item.price}}</span>
				<span>{{original_price ?'￥' : ''+item.original_price}}</span>
			</text>
		</view>
	</view>
</template>

<script>
	export default{
		name:'BookList',
		props:['list'],
		data(){
			return {
				// list:[
				// 	{
				// 		src:'../../static/logo.png',
				// 		title:'格列佛游记',
				// 		original_price:'16.90',
				// 		price:'免费'
						
				// 	},
				// 	{
				// 		src:'../../static/logo.png',
				// 		title:'西游记',
				// 		original_price:'16.90',
				// 		price:'0.99'
						
				// 	},
				// 	{
				// 		src:'../../static/logo.png',
				// 		title:'西游记',
				// 		original_price:'16.90',
				// 		price:'0.99'
						
				// 	}
				// ]
			}
		}
		
	}
</script>

<style lang="scss" scoped>
	.book-list-content{
		width: 100%;
		.list{
			width: 30%;
			margin: 0 5px;
			display: inline-block;
			text-align: center;
			image{
				width: 50%;
				height: 100px;
			}
		}
	}
</style>
