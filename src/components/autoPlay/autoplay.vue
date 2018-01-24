<template>
	<div>
		<swiper class="box-container" :options="swiperOption"  ref="myRdsa" @mouseover.native="stopPlay" @mouseout.native="Play">                           
            <swiper-slide v-for="i in autoData" class="img-box" @mouseover.native="stopPlay" @mouseout.native="Play">            	           		
	            	<div v-for="v in i.ImgUrl" class="img-item-box">
	               		<img :src="v" />
	               </div> 	               	            	               	                                                 	              	
            </swiper-slide>   
            <div class="swiper-pagination" slot="pagination" id="shousdfasdf"></div>
        </swiper>        
    </div>    
</template>

<script>
	import { swiper, swiperSlide } from 'vue-awesome-swiper'
	require ("../../assets/css/swiper.css")

export default {
		data () {
		    return {	    	 
			           
	          	/*swiperOption: {  
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
	          	}*/
	                
		    }
	  },	  
	  props:["swiperOption","autoData"],
	   components: {  
            swiper,  
            swiperSlide  
        },
        computed: {   
            swiper() {             	
              return this.$refs.myRdsa.swiper;  
            }  
        },
        methods:{  
        	one(){
        		console.log(this.dataAuto)
        	},
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
	.img-box{
		overflow: hidden;
		padding-bottom: 40px;
	}
	.img-item-box{
		float: left;
	}
	.img-item-box img{
		display: block;
		width: 184px;
	}
	#shousdfasdf>.swiper-pagination-bullet{
		width: 20px;
		height: 20px;		
	}
	#shousdfasdf>.swiper-pagination-bullet-active{
		background: pink;
	}
</style>