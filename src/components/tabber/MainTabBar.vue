<template>
	<tab-bar>
			<tab-bar-item path="/home" activeColor="#F6D95F">
				<img slot="item-icon" src="../../assets/img/tabbar/home_page.svg" alt="home">
				<img slot="item-icon-active" src="../../assets/img/tabbar/home_page1.svg" alt="home">
				<div slot="item-text">首页</div>
			</tab-bar-item>
			<tab-bar-item path="/category" activeColor="#D4237A">
				<img slot="item-icon" src="../../assets/img/tabbar/classification.svg" alt="home">
				<img slot="item-icon-active" src="../../assets/img/tabbar/classification1.svg" alt="home">
				<div slot="item-text">分类</div>
			</tab-bar-item>
			<tab-bar-item path="/shopcart" activeColor="#D4237A">
				<img slot="item-icon" src="../../assets/img/tabbar/Shopping_Cart.svg" alt="home">
				<img slot="item-icon-active" src="../../assets/img/tabbar/Shopping_Cart1.svg" alt="home">
				<div slot="item-text">购物车</div>
			</tab-bar-item>
			<tab-bar-item path="/profile" activeColor="#D4237A">
				<img slot="item-icon" src="../../assets/img/tabbar/user.svg" alt="home">
				<img slot="item-icon-active" src="../../assets/img/tabbar/user1.svg" alt="home">
				<div slot="item-text">我的</div>
			</tab-bar-item>
	</tab-bar>
</template>

<script>
	import TabBar from './tabbar.vue'
	import TabBarItem from './tabbaritem.vue'
	
	export default{
		name:'MainTabBar',
		components:{
			TabBar,
			TabBarItem
		}
	}
</script>

<style>
	
</style>
