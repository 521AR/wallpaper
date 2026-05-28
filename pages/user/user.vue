<template>
	<view class=" user-layout pageBg">
		<!-- 头像区域 -->
		<view class="user-info">
			<view class="avator">
				<image src="/common/images/classify1.jpg"></image>
			</view>
			<view class="nickName">
				今天又白雪了
			</view>
			<view class="addr">
				河南省尉氏县
			</view>
		</view>
		<!-- 功能区 -->
		<view class="orders">
			<view class="list">
				<view class="row">
					<view class="left">
						<uni-icons type="download-filled" size="20" color="blue"></uni-icons>
						<view class="text">我的下载</view>
					</view>
					<view class="right">
						<view class="text">33</view>
						<uni-icons type="right" size="14"></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="star-filled" size="20" color="blue"></uni-icons>
						<view class="text">联系客服</view>
					</view>
					<view class="right">
						<view class="text">66</view>
						<uni-icons type="right" size="14"></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="notification-filled" size="20" color="blue"></uni-icons>
						<view class="text">更新订阅</view>
					</view>
					<view class="right">
						<view class="text">20</view>
						<uni-icons type="right" size="14"></uni-icons>
					</view>
				</view>
			</view>
		</view>
		<view class="orders">
			<view class="list">
				<view class="row">
					<view class="left">
						<uni-icons type="flag-filled" size="20" color="blue"></uni-icons>
						<view class="text">常见问题</view>
					</view>
					<view class="right">
						<view class="text">15</view>
						<uni-icons type="right" size="14"></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="phone-filled" size="20" color="blue"></uni-icons>
						<view class="text">联系客服</view>
					</view>
					<view class="right">
						<view class="text">26</view>
						<uni-icons type="right" size="14"></uni-icons>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.user-layout{
		.user-info{
			padding: 50rpx 0 50rpx 0;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			.avator{
				image{
					width: 160rpx;
					height: 160rpx;
					border-radius: 50%;
				}
				
			}
			.nickName{
				font-size: 60rpx;
				color: #555;
				padding: 20rpx 0 20rpx 0;
			}
			.addr{
				font-size: 40rpx;
				color: #aaa;
			}
		}
		.orders{
			margin: 50px 30rpx;
			//border: 1px solid red;
			border-radius: 10rpx;
			box-shadow: 0 0 30rpx rgba(0,0,0,0.25);
			.list{
				.row{
					height: 100rpx;
					padding: 0 30rpx;
					border-bottom: 1px solid rgba(0,0,0,0.25);
					&:last-child{border-bottom: 0}
					display:flex;
					justify-content: space-between;
					align-items: center;
					.left{
						display: flex;
						align-items: center;
						.text{
							font-size :28rpx;
							color: #666;
							padding-left: 20rpx;
						}
					}
					.right{
						display: flex;
						align-items: center;
						.text{
							font-size: 24rpx;
							color: #aaa;
						}
					}
				}
			}
		}
	}
</style>
