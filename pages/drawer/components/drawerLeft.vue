<template>
	<myp-drawer ref="drawer-left" pos="left" standout="32rpx" width="600rpx" @overlayClicked="hide">
		<view class="dl">
			<menu-view></menu-view>
			<view style="width: 32rpx;"></view>
		</view>
	</myp-drawer>
</template>

<script>
	import menuView from './menuView.vue'
	
	export default {
		components: {
			menuView
		},
		methods: {
			hide(duration) {
				this.$refs['drawer-left'].hide(duration)
			},
			show(duration) {
				this.$refs['drawer-left'].show(duration)
			}
		}
	}
</script>

<style lang="scss" scoped>
	.dl {
		width: 600rpx;
		flex: 1;
		/* #ifndef APP-NVUE */
		display: flex;
		box-sizing: border-box;
		/* #endif */
		flex-direction: row;
		flex-wrap: nowrap;
		background-color: $myp-color-primary;
	}
</style>
