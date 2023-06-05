<template>
	<view class="content">
		<image class="logo" src="/static/logo.png" @click="showLoading"></image>
		<view class="text-area">
		</view>
	</view>
</template>

<script setup>
	const showLoading = () => {
		
		// #ifdef APP
		// 开启loading
		uni.navigateTo({
			url:"/pages/loading/loading"
		})
		// 模拟真实场景，3秒后关闭loading，
		setTimeout(()=>{
			uni.navigateBack()
		},3000)
		// #endif
		
		// #ifdef H5
		uni.showLoading()
		// #endif
	}
</script>

<style lang="scss">
	.uni-toast {
		background-color: #000;

		.uni-loading {}
	}











	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>