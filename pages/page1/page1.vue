<template>
	<view>
		<scroll-view class="bac" >
			<view class="ina" @click="goin(item)">
				<view class="left">
					<image src="https://i.loli.net/2021/02/19/vYXk2Wn1jB5IUZK.jpg"></image>
				</view>
				<view class="right">
					<h3>农家大西瓜</h3>
					<p>神奇农家大西瓜，点击在线观看。 -拼多多</p>
				</view>
			</view>
			<view class="ina" @click="goin(item)">
				<view class="left">
					<image src="https://i.loli.net/2021/02/19/vYXk2Wn1jB5IUZK.jpg"></image>
				</view>
				<view class="right">
					<h3>农家大草莓</h3>
					<p>神奇农家大草莓，点击在线观看。 -bilibili</p>
				</view>
			</view>
			<view class="ina" @click="goin(item)">
				<view class="left">
					<image src="https://i.loli.net/2021/02/19/vYXk2Wn1jB5IUZK.jpg"></image>
				</view>
				<view class="right">
					<h3>农家大红薯</h3>
					<p>神奇农家大红薯，点击在线观看。 -虎牙</p>
				</view>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad(){
			
		},
		onReady(){
			 this.videoContext=uni.createVideoContext('myVideo',this);
			            if(this.index===0){
			                setTimeout(()=>{
			                    this.videoContext.play();
			                },150)
			            }
		},
		methods: {
			goin(ur) {
				uni.navigateTo({
					url:"../page5/page5?url="+"https://www.baidu.com"
				})
			}
		}
	}
	

</script>

<style>
	.bac{
		background-color: #C8C7CC;
	}
	.ina{
		display: block;
		height: 300rpx;
		width: 100%;
		background-color: #ecf0f1;
		margin-bottom: 2rpx;
	}
	.left{
		display:inline-block;
		float: left;
		height:250rpx;
		width: 300rpx;
		margin-top: 25rpx;
		margin-left: 5rpx;
	}
	.left image{
		height: 100%;
		width: 100%;
	}
	.right{
		display:inline-block;
		float: left;
		height:250rpx;
		width: 440rpx;
		margin-top: 30rpx;
		margin-left: 5rpx;
	}
</style>
