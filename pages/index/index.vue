<template>
	<view class="home">
		<scroll-view scroll-x class="nav-scroll">
			<view class="item" v-for="(item,index) in navTabs" :key="index" :class="item.actived==true ?'actived':''" @click="changeNavTab(index)">
				{{item.name}}
			</view>
		</scroll-view>
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
				navTabs: [{
						name: '国内',
						actived: true
					},
					{
						name: '国外',
						actived: false
					},
					{
						name: '马鞍山',
						actived: false
					},
					{
						name: '花山区',
						actived: false
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			changeNavTab(activeIndex){
				this.navTabs.forEach((row,i)=>{
					row.actived=false
					if(activeIndex==i) row.actived=true
				})
			}	
		}
	}
</script>

<style lang="less" scoped>
	.nav-scroll {
		height: 100rpx;
		background-color: #F7F8FA;
		white-space: nowrap;
		position: fixed;
		top: var(--window-top);
		left: 0;
		z-index: 10;

		/deep/ ::-webkit-scroolbar {
			width: 4px !important;
			height: 1px !important;
			overflow: auto !important;
			background: transparent !important;
			-webkit-appearance: auto !important;
			display: block;
		}

		.item {
			font-size: 30rpx;
			display: inline-block;
			line-height: 100rpx;
			padding: 0 30rpx;
			color: #333;
		}
		.item.actived{
			color:#31c27c;
		}
	}

	.content {
		padding: 30rpx;
		padding-top: 70px;

		.row {
			border-bottom: 1px dotted #efefef;
			padding: 15rpx 0;
		}
	}
</style>