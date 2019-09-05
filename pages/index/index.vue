<template>
	<view>
		<button type="primary" style="margin: 10upx;" @click="onHandleCanvasAPI">CanvasAPI</button>
		<button type="primary" style="margin: 10upx;" @click="onHandleWebGL">CanvasWebGL</button>
		<button type="primary" style="margin: 10upx;" @click="onHandleAnimation">Animation</button>
	</view>
</template>
<script>
	export default {
		data() {
			return {
			}
		},
		onLoad() {
		},
		methods: {
			onHandleWebGL() {
				uni.navigateTo({
					url:"../canvas/webGL"
				})
			},
			onHandleCanvasAPI() {
				uni.navigateTo({
					url:"../canvas/canvas"
				})
			},
			onHandleAnimation (){
				uni.navigateTo({
					url:"../canvas/animation"
				})
			},
		}
	}
</script>
<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
