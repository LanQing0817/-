<template>
	<view class="news-item">
		<view class="pic">
			<image :src="item.picurl" alt="" mode="aspectFill"></image>
		</view>
		<view class="text-content">
			<view class="title" title="fuck you">{{item.title}}</view>
			<view class="info" v-if="!item.lookTime">
				<text class="author-name">{{item.author}}</text>
				<text class="flow-num">{{item.hits}}浏览</text>
			</view>
			<view class="info" v-else>
				<text class="time">浏览时间:{{item.lookTime}}</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "NewsItem",
		props: {
			item: {
				type: Object,
				default () {
					return {
						title: "组件内默认的标题",
						author: '张三',
						hits: 668,
						picurl: "../../static/兰青帅照.jpg",
						lookTime:'2024-2-4 21:00:00'
					}
				}
			}
		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="less">
	.news-item {
		display: flex;
		justify-content: flex-start;

		.pic {
			width: 260rpx;
			height: auto;

			image {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}

		.text-content {
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			padding-left: 20rpx;

			.title {
				font-size: 38rpx;
				color: #333;
				display: -webkit-box;
				overflow: hidden;
				text-overflow: ellipsis;
				-webkit-line-clamp: 2;
				-webkit-box-orient: vertical;
				line-height: 1.5em;
				height: calc(2 * 1.5em);
			}

			.info {
				margin-top: 38rpx;
				font-size: 26rpx;
				color: #999;

				.author-name {
					margin-right: 20rpx;
				}
			}
		}
	}
</style>