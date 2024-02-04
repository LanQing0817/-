<template>
	<view class="home">
		<scroll-view scroll-x class="nav-scroll">
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
			<view class="item">国内</view>
		</scroll-view>
		<view class="content">
			<div class="row">每一行的新闻</div>
		</view>
	</view>
</template>

<script>
	export default {
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

<style lang="less" scoped>
.nav-scroll{
	height: 100rpx;
	background-color: #F7F8FA;
	white-space: nowrap;
	/deep/ ::-webkit-scroolbar{
		width: 4px !important;
		height: 1px !important;
		overflow: auto !important;
		background:transparent !important;
		-webkit-appearance: auto !important;
		display: block;
	}
	.item{
		font-size:30rpx;
		display: inline-block;
		line-height: 100rpx;
		padding: 0 30rpx;
		color: #333;
	}
}
	
</style>
