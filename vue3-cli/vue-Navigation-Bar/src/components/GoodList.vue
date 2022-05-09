<template>
	<div name="show">
		<ul class="goodList">
			<li v-for="good in list">
				<img v-bind:src="good.img">
				<p>{{good.goodName}}</p>
			</li>
		</ul>
	</div>
</template>
<style type="text/css">
	.goodList li{
		list-style: none;
		width: 170px;
		float: left;
		height: 170px;
		color: red;
		font-size: 9px;
		margin-bottom: 5px;
	}
	.goodList img{
		width: 150px;
		height: 150px;
	}
</style>
<script type="text/javascript">
	export default{
		name:"show",
		data(){
			var _this=this;
			var url="";
			if(_this.goodId==1){
				url="json/bjb.json";
			}else if(_this.goodId==2){
				url="json/sj.json";
			}else if(_this.goodId==3){
				url = "json/fz.json"
			}else{
				url="json/bjb.json";
			}
			this.$http.get(url).then(function(res){
				_this.list=res.data;

			})
			return{
				list:[]
			}
		},
		props:{
			goodId:Number
		},
		watch:{
			goodId(){
				var _this=this;
				var url="";
			if(_this.goodId==1){
				url="json/bjb.json";
			}else if(_this.goodId==2){
				url="json/sj.json";
			}else if(_this.goodId==3){
				url="json/fz.json";
			}
			this.$http.get(url).then(function(res){
				_this.list=res.data;

			})
			return{
				list:[]
			}
			}
			
		}
	}
</script>