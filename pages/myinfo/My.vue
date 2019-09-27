<template>
	<view>
		<view class="user">
			<view class="user-avatar">
				<cmdAvatar shape="circle" src="../../static/logo.png"></cmdAvatar>
				<text>名字</text>
			</view>
			<view class="user-info">
				<uniGrid class="user-info-grid" :column="3" :show-border="false" :square="false">
					<uniGridItem class="user-info-grid-item" v-for="data in navbar">
						<text>{{data.num}}</text>
						<text>{{data.title}}</text>
					</uniGridItem>
				</uniGrid>
			</view>
			<view class="user-list">
				<uniList class="user-uni-list" v-for="item in list">
					<uniListItem :title="item.title" :thumb="item.imgsrc"></uniListItem>
				</uniList>
			</view>
		</view>
	</view>
</template>

<script>
	import uniList from '../../components/uni-list/uni-list.vue'
	import uniListItem from '../../components/uni-list-item/uni-list-item.vue'
	import cmdAvatar from '../../components/cmd-avatar/cmd-avatar.vue'
	import uniGrid from '../../components/uni-grid/uni-grid.vue'
	import uniGridItem from '../../components/uni-grid-item/uni-grid-item.vue'
	export default{
		name:'My',
		components:{uniList,uniListItem,cmdAvatar,uniGrid,uniGridItem},
		data(){
			return {
				title:'My',
				list:[{
					title:'我的账户',
					imgsrc:'../../static/icon/my/account_book_icon.svg'
				},
				{
					title:'笔记',
					imgsrc:'../../static/icon/my/label.svg',
				},
				{
					title:'分享',
					imgsrc:'../../static/icon/my/share.svg',
				},
				{
					title:'设置',
					imgsrc:'../../static/icon/my/set.svg',
				},
				],
				navbar:[{
					num:'12',
					title:'书单',
				},
				{
					num:'0',
					title:'评论',
				},
				{
					num:'23',
					title:'点赞',
				}]
			}
		}
	}
</script>

<style lang="scss">
	.user{
		background: #F5F7FC;
		.user-avatar{
			padding: 25px;
			background: #538EFB;
			display: flex;
			uni-text{
				margin: auto 20px;
				font-size: 18px;
				color: #fff;
				font-family: "微软雅黑";
			}
		}
		.user-info{
			width: 100%;
			text-align: center;
			padding-bottom: 10px;
			.user-info-grid{
				width: 80%;
				background: #fff;
				margin: -4% 10% 10px 10%;
				border-radius: 4px;
				padding: 5px 0;
				.user-info-grid-item{
					width: 33% !important;
				}
			}
		}
		.user-list{
			.uni-list:before{
				transform: 0 !important;
				background: #fff !important;
			}
			.uni-list:after{
				// transform: 0 !important;
				background: #fff;
			}
		}
	}
</style>
