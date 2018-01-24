<template>
  <div id="app"> 		
      <Header></Header>
      <Maue></Maue>      
      <Main></Main>
  </div>
</template>

<script>
	import Header from "./components/header.vue";
	import Maue from "./components/maue.vue";
	import Main from "./components/main.vue";
	export default {
	  data () {
	    return {
	      msg: 'Welcome to Your Vue.js App'
	    }
	  },
	  components:{
	  	Header,
	  	Maue,
	  	Main	  	
	  }
	}
</script>

<style>
	/*@import url("assets/css/index.css");*/
</style>
