<template>
	<div class="main">
		<div class="shop-auto-paly-list">
			<div class="shop-auto-paly-item">
				<h2><span>辞旧迎新</span>喜迎元旦</h2>
				<AutoPlay :swiperOption="swiperOption1" :autoData="autoData1"></AutoPlay>
			</div>
			<div class="shop-auto-paly-item">
				<h2><span>温暖畅享价</span>暖冬特惠</h2>
				<AutoPlay :swiperOption="swiperOption2" :autoData="autoData2"></AutoPlay>
			</div>
			<div class="shop-auto-paly-item">
				<h2><span>让利“更”疯狂</span>劲爆低价</h2>
				<AutoPlay :swiperOption="swiperOption3" :autoData="autoData3"></AutoPlay>
			</div>
		</div>		
	</div>
</template>
<script>
	import AutoPlay from "./autoPlay/autoplay.vue"
	export default {
		data () {
		    return {	    	 
				    list:[	
					      [
						      {
						      	imgId:1,
						      	ImgUrl:[require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg")]
						      },
						      {
						      	imgId:2, 
						      	ImgUrl:[require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg")]
						      },
						      {
						      	imgId:3, 
						      	ImgUrl:[require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg"),require("../assets/img/7.jpg")]
						      	}
						  ],
					      [
						      {imgId:1, ImgUrl:[require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg")]},
						      {imgId:2, ImgUrl:[require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg")]},
						      {imgId:3, ImgUrl:[require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg"),require("../assets/img/8.jpg")]}
						  ],
					      [
						      {imgId:1, ImgUrl:[require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg")]},
						      {imgId:2, ImgUrl:[require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg")]},
						      {imgId:3, ImgUrl:[require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg"),require("../assets/img/9.jpg")]}
						  ]
		          	],		          	
		          	swiperOption1: {  
		      			  notNextTick: true,
				          autoplay:{
				          	delay:2000,
				          	stopOnlassSlide:false,
				          	disabbleOnInteraction:false
				          },				         
						  pagination: {
						    el: '.swiper-pagination',
						    clickable :true,
						  }
		          	},
		          	swiperOption2: {  
		      			  notNextTick: true,
				          autoplay:{
				          	delay:4000,
				          	stopOnlassSlide:false,
				          	disabbleOnInteraction:false
				          },				         
						  pagination: {
						    el: '.swiper-pagination',
						    clickable :true,
						  }
		          	},
		          	swiperOption3: {  
		      			  notNextTick: true,
				          autoplay:{
				          	delay:6000,
				          	stopOnlassSlide:false,
				          	disabbleOnInteraction:false
				          },				         
						  pagination: {
						    el: '.swiper-pagination',
						    clickable :true,
						  }
		          	},
		    }
		},
		computed :{
			autoData1:function(){			
				return 	this.list[0]					
			},
			autoData2:function(){				
				return 	this.list[1]					
			},
			autoData3:function(){				
				return 	this.list[2]					
			}
		},
		components: {  
            AutoPlay
        },
	}
</script>

<style>
	.main{
		width: 1190px;
		margin: 0 auto;
		margin-top: 20px;
		overflow: hidden;
	}
	.shop-auto-paly-list{
		padding-left: 3px;
	}
	.shop-auto-paly-item{
		float: left;
		width: 390px;
		padding-right: 5px;
	}
	.shop-auto-paly-item h2{
		height: 52px;
		line-height: 52px;
		padding: 0 20px;
		color: #FFF;
	}
	.shop-auto-paly-item h2 span{
		float: right;
		font-size:12px;
	}
	.shop-auto-paly-item:nth-of-type(1) h2{
		background: #1d4ede;
	}
	.shop-auto-paly-item:nth-of-type(2) h2{
		background: #f7051a;
	}
	.shop-auto-paly-item:nth-of-type(3) h2{
		background: #03bb2c;
	}
</style>