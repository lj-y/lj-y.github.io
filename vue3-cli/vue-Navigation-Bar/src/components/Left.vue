<template>
	<div>
		<div class="title">热门推荐</div>
		<ul class="menu">
			<li @click='menu1'>电脑</li>
			<li @click='menu2'>手机</li>
			<li @click='menu3'>服装</li>
			<li @click='menu4'>学习用品</li>
			<li>办公用品</li>
			<li>旅游用品</li>
			<li>游戏卡通</li>
			<li>玩具</li>
			<li>书籍</li>
		</ul>
	</div>
</template>
<style type="text/css">
	.title{
		width: 150px;
		height: 50px;
		line-height: 50px;
		color: red;
	}
	.menu li{
		list-style: none;
		height: 50px;
		line-height:50px;
		margin-bottom: 2px;
		background-color: #fff;
		cursor: pointer;
	}
</style>
<script type="text/javascript">
	import Msg from './msg.js'
	export default{
		methods:{
			menu1:function(){
				Msg.$emit("val","1")
			},
			menu2:function(){
				Msg.$emit("val","2")
			},
			menu3:function(){
				Msg.$emit("val","3")
			},
			menu4:function(){
				Msg.$emit("val","4")
			},
		}
	}
</script>