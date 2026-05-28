<template>
	<view class="main-layout" pageBg>
		<!-- 轮播图模块  -->
		<view class="banner">
		
			<swiper indicator-dots indicator-color="rgba(255,255,255,0.5)"
			indicator-active-color="#fff" autoplay circular>
				<swiper-item v-for="item in 3">
					<image src="/common/images/more.jpg" mode="aspectFill"> </image>
				</swiper-item>
			</swiper>
		</view>
		<!-- 公告模块 -->
		<view class="notice">
			<view class="left">
				<uni-icons type="sound-filled" size="20" color="#28b389"></uni-icons>
				<text>公告</text>
			</view>
			<view class="center">
				<swiper vertical autoplay interval="1500" duration="300" circular>
					<swiper-item v-for="item in 4">
						<navigator url="/pages/notice/detail">
							公告标题
						</navigator>
					</swiper-item>
				</swiper>
			</view>
			<view class="right">
				<uni-icons type="right" size="16" color="#333"></uni-icons>
			</view>
		</view>
		<!-- 每日推荐  recommend-->
		<view class="recommend">
			<common-title>
				<template #title>每日推荐</template>
				<template #custom>
					<view class="date">
						<uni-icons type="calendar" size="18" color="#28b389"></uni-icons>
						<text>
							<!-- yyyy-MM-dd -->
							<uni-dateformat :date="Date.now()" format="yyyy-MM-dd"></uni-dateformat>
						</text>
					</view>
				</template>
			</common-title>
			<view class="content">
				<scroll-view scroll-x>
					<view class="box" v-for="item in 8">
						<image src="/common/images/preview1.jpg" mode="aspectFill"></image>
					</view>
				</scroll-view>
			</view>
		</view>
		<!-- 专题精选 theme(主题)-->
		<view class="theme">
			<common-title>
				<template #title>
					专题精选
				</template>
				<template #custom>
					<navigator url="/pages/classlist/classlist" class="more">More+</navigator>
				</template>
			</common-title>
			<view class="content">
				<theme-item v-for="item in 8"></theme-item>
				<theme-item :isMore="true"></theme-item>
			</view>
		</view>
		
		
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.main-layout{
		.banner{
			width: 750rpx;
			padding: 30rpx 0;
			swiper{
				width: 750rpx;
				height: 340rpx;
				swiper-item{
					width: 100%;
					height: 100%;
					padding: 0 30rpx;
					image{
						width: 100%;
						height: 100%;
						border-radius: 10rpx;
					}
				}
			}
		}
		.notice{
			background: #f7f7f7;
			border-radius: 41rpx;//要超过高的一半，会出现胶囊一样的边框
			width: 690rpx;
			height: 80rpx;
			margin: 0 auto;
			display: flex;
			line-height: 80rpx;
			.left{
				width: 140rpx;
				display: flex;
				align-items: center;
				justify-content: center;
				text{
					color: #28b389;
					font-weight: 600;
					font-size: 28rpx;
				}
			}
			.center{
				flex: 1;
				swiper{
					height: 100%;
					swiper-item{
						height: 100%;
						font-size: 30rpx;
						color: #666;
						//文字超出去，进行省略
						overflow: hidden;
						white-space: nowrap;
						text-overflow: ellipsis;
					}
				}
			}
			.right{
				width: 70rpx;
				display: flex;
				align-items: center;
				justify-content: center;
			}
		}
		.recommend{
			padding-top: 50rpx;
			.date{
				text{
					color: #28b389;
					margin-left: 5rpx;
				}
			}
			.content{
				width: 720rpx;
				height: 440rpx;
				margin-left: 30rpx;
				margin-top: 30rpx;
				scroll-view{
					white-space: nowrap;//包含的元素不换行
					.box{
						margin-right: 15rpx;
						width: 200rpx;
						height: 440rpx;
						display: inline-block;//行级块元素
						image{
							border-radius: 10rpx;
							width: 100%;
							height: 100%;
						}
					}
					.box:last-child{margin-right: 30rpx;}
				}
			}
		}
		.theme{
			padding-top: 50rpx;
			.more{
				font-size: 32rpx;
				color: #888;
			}
			.content{
				margin-top: 30rpx;
				padding: 0 30rpx;
				//显示方式,网格布局
				display: grid;
				gap: 15rpx;//网格之间的间隙
				grid-template-columns: repeat(3,1fr);//网格的布局方式    一行三个图片
			}
		}
	}
</style>
