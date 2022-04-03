<template>
	<view class="conten">
		<swiper class="sw1" autoplay="true" duration="1000" circular="true" indicator-dots="true">
			<swiper-item  class="sw_item" v-for="(item,i) in sw_items" :key="i">
				<image class="sw_item_in" mode="scaleToFill" :src="item" @click="previewImg(i)"></image>
			</swiper-item>
		</swiper>
		<view class="icon_area">
			<view class="ic_items">
				<view class="ic_item_in" v-for="(item,i) in icons[0]" :key="i" @click="goin(i)">
					<image mode="scaleToFill" :src="icons[1][i]" ></image>
					<text>{{item}}</text>
				</view>
			</view>
		</view>
		
		<scroll-view class="news">
			<ul>
				<li v-for="(item,i) in news" :key="i">
					<text>{{item}}</text>
				</li>
			</ul>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				sw_items: ["https://i.loli.net/2021/02/19/vYXk2Wn1jB5IUZK.jpg",
				"https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa0.att.hudong.com%2F30%2F29%2F01300000201438121627296084016.jpg&refer=http%3A%2F%2Fa0.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1615522221&t=9ac6b05e7e7033a7ea4eae38f51aeb8a",
				"https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa2.att.hudong.com%2F27%2F81%2F01200000194677136358818023076.jpg&refer=http%3A%2F%2Fa2.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1615522221&t=c80a9a46b584dd19434155a49a7f03d4",
				],
				icons:[["农餐","农宿","农游","农品","农玩","农场","VR看房"],
				["../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png",
				"../../static/icon_main/basket_.png"
				]],
				news: ["","应用介绍:农+APP是一款通过“搭建平台”+直播的方式，完成使消费者方便快捷获取乡村旅游信息功能的农业服务类APP，用于满足城市居民对休闲农业吃住行和生态农副产品的消费需求。用户通过手机APP自动定位，即可在农餐、农宿、农游、农品、农玩、农场分类中自由选择，用户还可通过观看在线直播和VR看房的方式去选择舒适的旅游场所。"]
			}
		},
		onLoad() {
		},
		onPullDownRefresh() {
			
			uni.stopPullDownRefresh()
		},
		methods: {
			previewImg(i) {
				var that = this
				uni.previewImage({
					current: that.sw_items[i],
					urls:that.sw_items,
					loop:true,
					indicator:'default'
				})
			},
			goin(i) {
				if(i == 0){
					console.log(i);
					uni.navigateTo({
						url:'../page3/page3'
					});
				}
				if(i == 1){
					console.log(i);
					uni.navigateTo({
						url:'../page3/page3'
					});
				}
				if(i == 2){
					console.log(i);
				}
				if(i == 3){
					console.log(i)
				}
				if(i == 4){
					console.log(i)
				}
				if(i == 5){
					console.log(i)
				}
				if(i == 6){
					console.log(i);
					uni.navigateTo({
						url:'../page4/page4'
					});
				}
				if(i == 7){
					console.log(i)
				}
				if(i == 8){
					console.log(i)
				}
				if(i == 9){
					console.log(i)
				}
			}
		}
	}
</script>

<style>
	@import url("./ic.css");
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.sw1 {
		height: 450rpx;
		width: 100%;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.sw_item,.sw_item_in{
		width: 100%;
	}
</style>
