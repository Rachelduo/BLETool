<template>
	<view class='btn-box' :style="{color:color}" @click="OnClick">
		<slot></slot>
	</view>
</template>

<script>
	export default {
		name:"btn",
		props:{
			color:{
				type:String,
				default:'000'
			}
		},
		data(){
			return{};
		},
		methods:{
			OnClick(){
				console.log('我被点击了')
				this.$emit('change',this.color)
			}
		}
		
	}
</script>

<style>
     .btn-box{
		 width:200px;
		 height:100px;
		 text-align:center;
		 line-height:100px;
		 background-color: aqua;
		
	 }
</style>