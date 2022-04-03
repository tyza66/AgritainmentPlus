<template>
	<view>
		<web-view class="in" :src="url" scrolling="no"></web-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				url:null
			}
		},
		onLoad(thing){
			this.url = thing.url
		},
		methods: {
			
		}
	}
</script>

<style>
	.in{
		width: 100%;
		height: 100%;
	}
</style>
