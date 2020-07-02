<template>
  <div id="app">
    <router-view />
    <footer-guide v-show="$route.meta.showFooter" />
  </div>
</template>

<script>
	import FooterGuide from "./components/FooterGuide/FooterGuide.vue";
	// 先在App.vue中引入封装的接口函数
	import { reqFoodCategorys } from "./api";
	// 然后再调用接口，测试打印数据
	export default {
 	  mounted() {
		this.$store.dispatch('getAddress')
  	},
  	components: {
    	FooterGuide
 	 }
	};
</script>
<style lang="stylus" rel="stylesheet/stylus">
.app {
  width: 100%;
  height: 100%;
  background: #f5f5f5;
}
</style>