<template>
	<div class="header">
		<div class="header-left">
			<div class="iconfont icon-fanhui back-icon"></div>
		</div>
		<div class="header-input">
			<span class="iconfont icon-sousuo"></span>
		输入景点\城市\游玩主题</div>
		<router-link to='/city'>
			<div class="header-right">
				{{this.city}}
				<span class="iconfont icon-jiantou arrow-icon"></span>
			</div>
		</router-link>	
	</div>
</template>
<script>
import { mapState } from 'vuex'
export default{
	name:'HomeHeader',
	computed: {
		...mapState(['city'])
	}
}
</script>
<style lang="stylus" rel="stylesheet/stylus">
@import '~styles/varibles.styl'
.header
	line-height:.86rem
	display:flex
	background:$bgColor
	color:#fff
	.header-left
		width:.64rem
		float:left
		.back-icon
			text-align:center
			font-size:.4rem
	.header-input
		flex:1
		height:0.64rem
		line-height:0.64rem
		margin-top:.12rem
		margin-left:.2rem
		background:#fff
		border-radius:.1rem
		color:#ccc
	.header-right
		min-width:1.04rem
		padding:0 .1rem
		float:right
		text-align:center
		color:#fff
		.arrow-icon
			margin-left:-.04rem
			font-size:.24rem
</style>