<template>
	<view class="common-title">
		<!-- 使用插槽方式来实现，同样的组件显示不同的内容 -->
		<view class="name">
			<slot name="title"></slot>
		</view>
		<view class="custom">
			<slot name="custom"></slot>
		</view>
	</view>
</template>

<script setup>
	defineProps(['name','date'])
	
</script>

<style lang="scss" scoped>
	.common-title{
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0 30rpx;
		.name{
			font-size: 40rpx;
		}
	}
</style>