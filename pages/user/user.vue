<template>
	<view class="user-center">
		<div class="top">
			<image src="../../static/history.png"></image>
			<div class="text">浏览历史</div>
		</div>
		<view class="content">
			<view class="row" v-for="item in 10">
				<NewsItem></NewsItem>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="less">
.top{
	padding: 20rpx 0;
	display: flex;
	flex-direction: column;
	align-items: center;
	background-color: #f7f7f7;
	image{
		width: 100rpx;
		height: 100rpx;
	}
	.text{
		margin-top:20rpx;
	}
}
.content{
	padding: 30rpx;
	.row{
		border-bottom: 1px dotted #efefef;
		padding:15rpx 0;
	}
}
</style>
