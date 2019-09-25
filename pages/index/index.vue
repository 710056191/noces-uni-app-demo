<template>
	<view class="main">
	<view class="content">
		<view class="text-area">
			<icon type="search" size="16" color="blue"></icon>
			<input class="text-area-input" type="text" confirm-type="search" placeholder="找书籍,搜评论" />
		</view>
		<view >
			<image src="../../static/logo.png"></image>
		</view>
		<view class="content-nav">
			<uniGrid :column="4" :show-border="false" :square="false">
				<uniGridItem>
					<text class="uni-grid-icon-text" style="background: #6FB8F9;"><uni-icon class="iconfont icon_classification" style="color: #fff;">&#xe60b;</uni-icon></text>
					<text class="uni-grid-text">分类</text>
				</uniGridItem>
				<uniGridItem>
					<text class="uni-grid-icon-text" style="background: #77CD71;"><uni-icon class="iconfont icon-Book" style="color: #fff;">&#xe629;</uni-icon></text>
					<text class="uni-grid-text">畅读</text>
				</uniGridItem>
				<uniGridItem>
					<text class="uni-grid-icon-text" style="background: #FCA458;"><uni-icon class="iconfont icon_bookmark--fill" style="color: #fff;">&#xe69b;</uni-icon></text>
					<text class="uni-grid-text">推荐</text>
				</uniGridItem>
				<uniGridItem>
					<text class="uni-grid-icon-text" style="background: #FA6574;"><uni-icon class="iconfont icon-book2" style="color: #fff;">&#xe604;</uni-icon></text>
					<text class="uni-grid-text">书院</text>
				</uniGridItem>
			</uniGrid>
		</view>
		<view class="new">
			<view class="new-title">
				<h3>新手推荐</h3>
			</view>
			<view class="new-content">
				<view class="new-left">
					<image src="../../static/logo.png" style="width: 114px;height: 100px;"></image>
					<h5>经典畅销书</h5>
					<text>斑马人的生活</text>
				</view>
				<view class="new-right">
					<view class="new-right-top">
						<view>
							<h5>限时免费</h5>
							<text>感知</text>
						</view>
						<view>
							<image src="../../static/logo.png" style="width: 80px;height: 90px;"  />
						</view>
					</view>
					<view class="new-right-botoom">
						<view>
							<h5>限时免费</h5>
							<text>感知</text>
						</view>
						<view>
							<image src="../../static/logo.png" style="width: 80px;height: 90px;" />
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
	<view class="uni-flex uni-row btn-area">
		<uniGrid :column="3" :show-border="false" :square="false">
			<uniGridItem>
				<uni-icon class="iconfont icon-icon_study_fill">&#xebaf;</uni-icon>
				<text style="background: none;" >书城</text>
			</uniGridItem>
			<uniGridItem>
				<uni-icon class="iconfont icon-book">&#xe61f;</uni-icon>
				<text style="background: none;" >书架</text>
			</uniGridItem>
			<uniGridItem>
				<uni-icon class="iconfont icon-CN_taobaowangwang">&#xe65d;</uni-icon>
				<text style="background: none;" >我的</text>
			</uniGridItem>
		</uniGrid>
	</view>
	</view>
</template>

<script>
	
	import uniGrid from '@/components/uni-grid/uni-grid.vue'
	import uniGridItem from '@/components/uni-grid-item/uni-grid-item.vue'
	import uniIcon from '@/components/uni-icons/uni-icons.vue'
	export default {
		components:{uniGrid,uniGridItem,uniIcon},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	@import url("./index.scss");
	
</style>
