<template>
	<div class="container-fluid">
		<div class="navbar navbar-inverse">
			<router-link  to="/" class="navbar-brand">商店</router-link>
			<div class="navbar-right">
				<div class="navbar-text">
					<b>你的购物车</b>
					{{sum}} 件,￥{{total}}.00
				</div>
				<router-link to="/checkout" class="btn btn-default navbar-btn">checkout</router-link>
			</div>
		</div>
	</div>
</template>
<script type="text/javascript">
export default{
	computed:{
		total(){
			return this.$store.getters.total
		},
		sum(){
			return this.$store.getters.sum
		}
	}
}
</script>
<style>
.navbar-right{
	float: right !important;
	margin-right: 5px;
}
.navbar-text{
	margin-right: 10px;
}	
</style>