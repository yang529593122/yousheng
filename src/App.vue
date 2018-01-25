<template>
  <div id="app"> 		
      <Header></Header>
      <Maue></Maue>      
      <Main></Main>
      <life></life>
      <showbox></showbox>
      <showbox></showbox>
      <showbox></showbox>
      <showbox></showbox>
      <showbox></showbox>
  </div>
</template>

<script>
	import Header from "./components/header.vue";
	import Maue from "./components/maue.vue";
	import Main from "./components/main.vue";
	import Life from "./components/life.vue";
	import Showbox from "./components/common/showbox.vue";
	export default {
	  data () {
	    return {
	      msg: 'Welcome to Your Vue.js App'
	    }
	  },
	  components:{
	  	Header,
	  	Maue,
	  	Main,
	  	Life,
	  	Showbox
	  }
	}
</script>

<style>
	/*@import url("assets/css/index.css");*/
</style>
