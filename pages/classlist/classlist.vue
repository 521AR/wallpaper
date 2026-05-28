<template>
	<view class="classlist pageBg">
		<view class="content">
			<navigator url="/pages/preview/preview" v-for="item in 10">
				<image  src="/common/images/classify2.jpg" mode="aspectFill"></image>
			</navigator>
		</view>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.classlist{
		.content{
			display: grid;
			grid-template-columns: repeat(3,1fr);
			gap: 15rpx;
			padding: 15rpx;
			image{
				width: 100%;
				border-radius: 5rpx;
			}
		}
	}       
</style>
