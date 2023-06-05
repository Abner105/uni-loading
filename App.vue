<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	/* 	.uni-toast{
		background-color: #fff7f8;
		box-shadow: 0 0 10rpx pink;
		width: 160rpx;
		.uni-loading{
			background-image: none;
			border-radius: 50%;
			border-top: 16rpx pink solid;
		}
	} */
	.uni-toast {
		background-color: #000;
		box-shadow: 0 0 20rpx #000;

		.uni-loading {
			background-image: none;
			border: 2px #6572ff solid;
			animation: none;
			width: 70px !important;
			border-radius: 4px;
			height: 14px !important;
			position: relative;

			&::after {
				content: '';
				left: 0;
				position:absolute;
				display: inline-block;
				width: 20px;
				height: 10px;
				border-radius: 2px;
				background-color: #c1ff2f;
				animation: full 2s infinite;
			}

			@keyframes full {
				0% {
					width: 0;
				}
				100% {
					width: 67px;
				}
			}
		}
	}
</style>