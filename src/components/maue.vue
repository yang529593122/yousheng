<template>
	<div class="maue">
		<div class="maue-left">
			 
		</div>
		<div class="maue-right">
			<div class="maue-right-autoPlay">					
					<swiper class="box-container" :options="swiperOption"  ref="mySwiper" @mouseover.native="stopPlay" @mouseout.native="Play">                           
                        <swiper-slide v-for="item in list"> 
                            <img :src="item.img" class="index_img">
                        </swiper-slide>                        
                        <div class="swiper-pagination" slot="pagination"></div>
                        <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
                        <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
                    </swiper>  
			</div>
			<div class="maue-right-info">
					<div class="announcement">
							<h4>公告</h4>
							<ul>
								<li><a href="">百姓领购网线下及线上积分兑换</a></li>
								<li><a href="">百姓领购网商城招商函</a></li>
								<li><a href="">百姓领购网</a></li>
								<li><a href="">七天无理由退换服务</a></li>
							</ul>
						
					</div>
					<div class="helpList">						
						<h4>快捷导航</h4>
						<div class="con">
							<ul>
								<li><span></span><span>团购</span></li>
								<li><span></span><span>抢购</span></li>
								<li><span></span><span>优惠券</span></li>
								<li><span></span><span>积分</span></li>
								<li><span></span><span>资讯</span></li>
								<li><span></span><span>快递</span></li>
							</ul>
						</div>
					</div>
			</div>
		</div>
	</div>
</template>
<script>
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	require ("../assets/css/swiper.css")
	export default {
		data () {
	    return {	    	 
		    list:[	
			      {img: require('../assets/img/1.gif')},
		          {img: require('../assets/img/2.jpg')},
		          {img: require('../assets/img/3.jpg')}		          
          	],           
          	swiperOption: {  
      			  notNextTick: true,
		          autoplay:{
		          	delay:1000,
		          	stopOnlassSlide:false,
		          	disabbleOnInteraction:false
		          },
		          navigation: {
				    nextEl: '.swiper-button-next',
				    prevEl: '.swiper-button-prev'
				  },
				  pagination: {
				    el: '.swiper-pagination',
				    clickable :true,
				  },
          	}
                
	    }
	  },
	   components: {  
            swiper,  
            swiperSlide  
        },
        computed: {   
            swiper() {             	
              return this.$refs.mySwiper.swiper;  
            }  
        },
        methods:{
        	stopPlay(){
        		this.swiper.autoplay.stop()
        	},
        	Play(){
        		this.swiper.autoplay.start()
        	}
        }
        
		
	}
	
</script>
<style>	
	.maue{
		width: 1190px;
		height: 424px;
		
		margin: 0 auto;
	}
	.maue-left{
		float: left;
		width: 210px;
		height:424px ;
		
	}
	.maue-right{
		float: right;		
	}
	.maue-right-autoPlay{
		float: left;
		width: 760px;
		height: 424px;		
		margin-right: 10px;
	}
	.maue-right-autoPlay img{
		display: block;
		width: 100%;
	}
	.maue-right-info{
		float: left;
		width: 200px;
		height: 424px;
		
	}
	.announcement{
		height: 215px;
	}
	.announcement h4{
		    height: 40px;
		    padding: 0 10px;
		    line-height: 40px;
		    font-size: 14px;
		    color: #333;
		    font-family: Microsoft yahei;
		    border-bottom: 1px solid #eeeeec;
	}
	.maue-right-info{
		width: 200px;
	}
	.announcement ul li{
		   	 margin-top: 10px;
   			 line-height: 16px;
   			 color: #808080;
   			 font-size: 12px;   		
	}
	.announcement ul li a{
		text-decoration: none;
		color: #3c3c3c;
	}
	.announcement ul li a:hover{
		color:red;
	}
	.helpList h4{
		line-height: 40px;
	    font-size: 14px;
	    color: #333;
	    font-family: Microsoft yahei;
	    height: 40px;
	    padding: 0 10px;	    
	    font-size: 14px;
	    color: #333;
	    font-family: Microsoft yahei;
	    background: white;
	}
	.helpList .con{
		border: 1px solid #f0f0f0;
	    border-width: 1px 0 0 1px;
	    background: white;
	    overflow: hidden;
	}
	.helpList .con ul li{
		    width: 45px;
		    height: 66px;
		    float: left;
		    border: 1px solid #f0f0f0;
		    border-width: 0 1px 1px 0;
		    text-align: center;
		    padding-top: 15px;
	}
	.helpList .con ul li span{
		display: block;
	}
	.helpList .con ul li span:nth-of-type(1){
		    width: 28px;
		    height: 25px;
		    display: inline-block;		   
		    background: url(../assets/img/new-icn.png) no-repeat;		   
	}
	.helpList .con ul li:nth-of-type(1) span:nth-of-type(1){		   
		   background-position: 0 -340px;
	}
	.helpList .con ul li:nth-of-type(2) span:nth-of-type(1){				   		   
		    background-position: -38px -340px
	}
	.helpList .con ul li:nth-of-type(3) span:nth-of-type(1){		   
		     background-position: -79px -340px
	}
	.helpList .con ul li:nth-of-type(4) span:nth-of-type(1){		   
		    background-position: 0 -370px;
	}
	.helpList  .con ul li:nth-of-type(5) span:nth-of-type(1){		    
		    background-position: -38px -370px;
	}
	.helpList  .con ul li:nth-of-type(6) span:nth-of-type(1){		    
		    background-position: -81px -370px;
	}
	.helpList .con ul li span:nth-of-type(2){
		padding-top: 10px;
		font-size: 12px;
	}
</style>