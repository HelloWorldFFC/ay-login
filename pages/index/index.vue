<template>
	<view >
		<loginPassword :themeColor="themeColor" :logoUrl="logoUrl"  @loginFun="loginFun"></loginPassword>
		
	</view>
</template>

<script>
	import loginPassword from '@/components/ay-login/login-password.vue';
	export default {
		components: {
			loginPassword,

		},
		data() {
			return {
				themeColor : '#33CCCC',
				logoUrl:'https://cdn.pixabay.com/photo/2016/11/23/17/55/beach-1854072__340.jpg',
					
			}
		},
		onLoad() {
			let that = this;

		},

		methods: {
			loginFun(e){
				console.log('登录'+ JSON.stringify(e))
			},
		}
	}
</script>

<style lang="scss">
</style>
