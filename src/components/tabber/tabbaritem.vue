<template>
	<div class="tab-bar-item" @click="itemClick"> 
		<div v-if=" !isActive "><slot name="item-icon"></slot></div>
		<div v-else><slot name="item-icon-active"></slot></div>
		<div :style="activeStyle">
			<slot name="item-text"></slot>
		</div>
		
		<!-- <img src="../../assets/img/tabbar/home_page.svg"/>
		<div>首页</div> -->
	</div>
</template>

<script>
	export default{
		name:"TabBarItem",
		props:{
			path:String,
			activeColor:{
				type:String,
				default:'#D4237A'
			}
		},
		data(){
			return{
				//isActive:true
			}
		},
		//计算属性
		computed:{
			isActive(){
				// /home ->item1(/home) = true
				// /home ->item1(/category) = false
				// /home ->item1(/shopcart) = true
				// /home ->item1(/profile) = true
				return this.$route.path.indexOf(this.path) !== -1
			},
			activeStyle(){
				return this.isActive ? {color: this.activeColor} : {}
			},
		},
		methods:{
			itemClick(){
				// console.log("itemClick");
				this.$router.replace(this.path)
			}
		}
	}
</script>

<style>
	.tab-bar-item{
		flex: 1;
		height: 49px;
		text-align: center;
		font-size: 14px;
	}
	.tab-bar-item img{
		width: 24px;
		height: 24px;
		margin-top: 3px;
		vertical-align: middle;
	}
</style>
