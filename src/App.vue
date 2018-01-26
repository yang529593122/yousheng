<template>
  <div id="app"> 		
      <Header></Header>
      <Maue></Maue>      
      <Main></Main>
			<Footer></Footer>
  </div>
</template>

<script>
	import Header from "./components/header.vue";
	import Maue from "./components/maue.vue";
	import Main from "./components/main.vue";
	import Footer from "./components/footer.vue";
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
			Footer	  	
	  }
	}
</script>

<style>
	/*@import url("assets/css/index.css");*/
</style>
