<template>
	<view class="news-item">
		<view class="pic">
			<img src="../../static/兰青帅照.jpg" alt="" />
		</view>
		<view class="text-content">
			<view class="title" title="fuck you">默认的新闻标题 默认的新闻标题 默认的新闻标题 默认的新闻标题 默认的新闻标题</view>
			<view class="info">
				<text class="author-name">作者名称</text>
				<text class="flow-num">998浏览</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "NewsItem",
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
			width: 400rpx;
			height: auto;

			img {
				width: 100%;
				height: 100%;
				object-fit:cover;
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