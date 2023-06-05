<template>
	<view class="loading-wrapper">
		<image src="../../static/loading.gif" mode=""></image>
	</view>
</template>

<script setup>
	import { onBackPress } from "@dcloudio/uni-app"
	onBackPress((e) => {
		// 安卓禁用侧滑返回
		if(e.from==='backbutton'){
			return true
		}
	})
</script>

<style>
	page {
		height: 100%;
		width: 100%;
		/* 设置页面背景透明 */
		background: transparent;
	}
</style>
<style lang="scss">
	.loading-wrapper {
		height: 100%;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;

		image {
			width: 120rpx;
			height: 120rpx;
		}
	}
</style>