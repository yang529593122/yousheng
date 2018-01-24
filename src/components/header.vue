<template>
	<div class="header">
		 <div class="header-top-nav">
	 		<div class="header-top-nav-left">
	 			<ul>
	 				<li>商城首页</li>
	 				<li>欢迎光临！请<span>登录</span></li>	 				
	 				<li>免费注册</li>
	 			</ul>
	 		</div>
	 		<div class="header-top-nav-right">
 				<ul>
 					<li class="my-shop" @click="headerShowCity()"  :class="{ bg: isShowCity}">
 						我的商城
 						<div class="my-shop-info"  v-show="isShowCity">
 							<ul>
 								<li>待处理订单</li>
 								<li>咨询回复</li>
 								<li>我的订单</li>
 								<li>我的积分</li>
 							</ul>
 						</div>
 					</li>
 					<li>我的购物车</li>
 					<li class="my-shop" @click="headerShowCollect()" :class="{ bg: isCollect}">
 						我的收藏
 						<div class="my-shop-info"  v-show="isCollect">
 							<ul>
 								<li>收藏的商品</li>
 								<li>收藏的店铺</li>
 								
 							</ul>
 						</div>
 					</li>
 					<li>招商加盟</li>
 					<li>帮助中心</li>
 					<li class="my-shop" @click="headerShowNav()" :class="{ bg: isNav}">
 						网站导航
 						<div class="my-shop-info"  v-show="isNav">
 							<ul>
 								<li>待处理订单</li>
 								<li>咨询回复</li>
 								<li>我的订单</li>
 								<li>我的积分</li>
 							</ul>
 						</div>
 					</li>
 				</ul>
	 		</div>
		 </div>
		 <div class="header-top-search">
		 	<div class="header-logo">
		 		<img src="../assets/img/logo.png" alt="" />
		 	</div>
		 	<div class="header-search-input">
		 		<ul>
		 			<li>
		 				<span>宝贝</span>
		 				<span>店铺</span>
		 				<span>资讯</span>
		 				<span>供求</span>
		 			</li>
		 			<li>
		 				<input type="text" /><span>搜 索</span>
		 			</li>
		 			<li>
		 				<a href="">年货节</a>
		 				<a href="">皮衣</a>
		 				<a href="">海参</a>
		 				<a href="">大闸蟹</a>
		 				<a href="">羊奶粉</a>
		 			</li>
		 		</ul>
		 	</div>
		 	<div class="header-shop">
		 		<span>去购物车结算</span>
		 	</div>
		 </div>
		 <div class="header-top-bottom">
		 	<h3>全部商品分类 </h3>
		 	<ul>
		 		<li v-for="item in arr">{{item}}</li>
		 	</ul>
		 	<Tab></Tab>
		 </div>	
	</div>
</template>

<script>
	import Tab from "./header/tab.vue"
	export default {	 
	  data () {
	    return {	     
	      isShowCity:false, //我的显示隐藏开关
	      isCollect:false,
	      isNav:false,	     
	      arr:["首页","优惠券","抢购","团购","供求","店铺","资讯","积分商城"],	      	     
	    }
	  },
	   components:{
	   		Tab
	   },
	   created: function(){
	        this.$http.post('http://47.104.128.231:8082/shop_rest/rest/itemcat/list')
			  .then((response)=> {
			  	var jsons=response.data.data
			  	this.NavData=jsons;	
			  	for(var i=0;i<jsons.length;i++){
			  		this.itemDatas.push(jsons[i].i)
			  	}			  	
			  })
			  .catch(function (error) {
			    console.log(error)
			 });	       
	    },
	  methods:{
	  	headerShowCity(){	  		
	  		 this.isShowCity = !this.isShowCity;
	  	},
	  	headerShowCollect(){
	  		this.isCollect = !this.isCollect;
	  	},
	  	headerShowNav(){
	  		this.isNav = !this.isNav;
	  	},
	  	hhh(){
	  		
	  	}
	  }
	}
</script>

<style lang="scss">
	ul li{
		list-style: none;
		padding: 0 10px;
	}
	*{margin: 0;padding: 0;}	
	.header{
		width: 1190px;
		margin: 0 auto;
		
	}
	.header-top-nav{
		height: 34px;
		background: #f7f7f7;		
	}
	.header-top-nav-left{
		float: left;
	}
	
	.header-top-nav-right{
		float: right;
	}
	.header-top-nav ul li{
	  float: left;
	  width: 80px;
	  line-height:34px;
	  text-align: center;
	  font-size: 12px;	  
	}
	.header-top-nav-left ul li{
		padding: 0 5px;
		width: auto;
	}	
	.header-top-search{
		height: 105px;
		padding: 15px 0;
	}
	.header-logo,.header-search-input,.header-shop{
		float: left;
	}	
	.header-search-input{
	 	padding-left: 50px;
	 	padding-right: 100px;
	}
	.header-search-input ul li:nth-of-type(1){
		line-height: 20px;
	}
	.header-search-input ul li:nth-of-type(1) span{
		padding: 0 4px;
		color: #808080;
		font-size: 12px;
	}
	.header-search-input ul li:nth-of-type(2){
		border: 2px red solid;
		padding: 0;
		overflow: hidden;
	}
	.header-search-input ul li:nth-of-type(2) input:nth-of-type(1){
		height:28px;
		width: 380px;
		float: left;
	}
	.header-search-input ul li:nth-of-type(2) span{
		float: left;
		display: block;
		height: 100%;
		width: 85px;		
	    border: 0;
	    letter-spacing: 4px;
	    cursor: pointer;
	    color: #fff;
	    background-color: #f75364;	    
	    font: 400 16px/32px microsoft yahei;
	    overflow: hidden;
	    text-align: center;
	}
	.header-search-input ul li:nth-of-type(3) a{
		padding: 0 4px;
		color: #808080;
		font-size: 12px;
		text-decoration: none;
	}
	.header-search-input ul li:nth-of-type(3) a:hover{		
		color: red;		
	}
	.header .header-shop{		
	    margin-top: 20px;
	    background-color: white;	    
	    text-align: center;	 
        border: 1px solid #e3e3e3;
        height: 35px;
        padding: 0 10px 0 50px;
        background:#f7f7f7 url(../assets/img/carbg.jpg) 15px center no-repeat;               
	}	
	.header .header-shop span{				
	    display: block;
	    height: 30px;
	    width: 100%;
	    cursor: pointer;
	    line-height: 30px;
	    font-size: 12px;	   
	}	
	.my-shop{
		position: relative;
		text-align: center;
		
	}
	.my-shop-info{
		position: absolute;
		background: #fff;
		top: 34px;
		left: 0;		
	}
	.my-shop-info ul li{
		clear: both;
	}
	.bg{
		background-color: #fff;
	}
	.header-top-bottom{
		height: 40px;
		position: relative;
	}
	
	.header-top-bottom ul{
		float: left;
	}
	.header-top-bottom ul li{
		float: left;       
	}
	.header-top-bottom ul li a{
		display: block;
		padding: 0 20px 3px;
	    font: 16px/37px microsoft yahei;
	    color: black;
	    text-decoration: none;
	}
	.header-top-bottom ul li a:hover{
		border-bottom: 3px solid red;
		color: red;
		
	}
	.header-top-bottom h3{
		float: left;
		width: 210px;
		background: #3c3c3c;
		line-height: 40px;
		color: #fff;
		text-align: center;
		letter-spacing: 7px;
		position: relative;
	}
	.header-top-bottom h3 div{
		position: absolute;
		top:40px;	
	}
	.header-top-bottom h3 h6{
		background: red;
		width: 210px;
		border-bottom: 1px #fff dashed;
		height: 52px;
		line-height: 52px;
	}
	.header-top-bottom h3 h6 a{
		text-decoration: none;
		color: #fff;
		font-size: 18px;
		font-size: 18px;       
        font-weight: 400;
    	letter-spacing: 5px;
	}
	.header-top-bottom .navList-maue{
		width: 760px;
		height: 420px;
		position: absolute;
		right:-770px;
		background: green;
		z-index: 1000;
	}
	.maue-item{
		clear:both;
	}
	.header-top-bottom ul li{
		line-height: 40px;
	}
</style>