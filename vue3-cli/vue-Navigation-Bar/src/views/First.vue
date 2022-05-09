<template>
	<div class="main">
		<div class="left">
			<Left></Left>
		</div>
		<div class="right">
			<div class="top">
				<img src="img/title.jpg">
			</div>
			<div class="bottom">
				<Right></Right>
			</div>
		</div>
	</div>
</template>
<style type="text/css">
	*{
		padding: 0px;
		margin: 0px;
	}
	.main{
		margin:10px auto 50px;
		width: 1020px;
		/*background-color:#c5c5c5;*/
		height: 600px;
	}
	.top img{
		width: 850px;
		height: 250px;
	}
	.left{
		width: 150px;
		height: 600px;
		background-color: #f5f5f5;
		margin-right: 10px;
		float: left;
	}
	.right{
		width:850px;
		height: 600px;
		background-color: #f5f5f5;
		margin-left: 10px;
		float:left;
	}
</style>
<script type="text/javascript">
	import Left from '../components/Left.vue'
	import Right from '../components/Right.vue'
	export default{
		components:{
			Left,
			Right
		}
	}
</script>