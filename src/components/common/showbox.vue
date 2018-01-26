<template>
	<div class="showArae">
		<div class="showArae-tielt">
			<h4><span>1F</span> <span>服装区域</span></h4>
		</div>
		<div class="showArae-items">
			<div class="showArae-items-nav">
					<h5>分类</h5>
					<ul>
						<li>女装</li>
						<li>男装</li>
						<li>时尚内衣</li>
						<li>童装童鞋</li>
						<li>配饰</li>
						<li>潮流女包</li>
						<li>潮流男包</li>
						<li>功能箱包</li>
					</ul>
					<div>
						<img src="../../assets/20.jpg"  />
					</div>
			</div>
			<div class="showArae-imgs">
				<div>
					<img src="../../assets/21.jpg" />
				</div>
				<div>
					<img src="../../assets/22.jpg"  />
				</div>
			</div>
			<div class="showArae-imgs-items">
				<img :src="item" v-for="(item,index) in listUrl" :class="{ 'AnimationStart': index === isActive, 'AnimationEnd': index === isHide}" @mousemove="showAnimation(index)" @mouseleave="hideAnimation(index)"/>
			</div>
		</div>
		
	</div>
</template>

<script>
	
	export default{
		data(){
			return{
				listUrl:[
					require("../../assets/23.jpg"),
					require("../../assets/23.jpg"),
					require("../../assets/24.jpg"),
					require("../../assets/23.jpg"),
					require("../../assets/23.jpg")
				],
				isActive:0,
				isHide:0,								
			}
		},
		methods:{
			showAnimation(index){				
				 this.isActive = index;
			},
			hideAnimation(index){
				this.isHide = index;
			}
		}
	}
</script>

<style>
		
	.showArae{
		width: 1190px;
		margin: 10px auto;
	}
	.showArae-tielt{
		border-bottom:2px solid #ca4974 ;
	}
	.showArae-tielt h4{
		height: 48px;
		line-height: 48px;
	}
	.showArae-tielt h4 span{
		color: #ca4974;
		font-size: 18px;
	}
	.showArae-items{
		overflow: hidden;
	}
	.showArae-items-nav{
		float: left;
		width: 140px;
		margin-right: 30px;		
	}
	.showArae-items-nav h5{
		    font: 700 17px/16px microsoft yahei;
		    color: #c59d6c;
		    padding: 10px 0;
	}
	.showArae-items-nav ul{
		overflow: hidden;
	}
	.showArae-items-nav ul li{				
	    float: left;
	    width: 50px;
	    height: 40px;
	    line-height: 40px;	    
	    border-bottom: 1px dashed #f1e1cc;
	    white-space: nowrap;
	    text-overflow: ellipsis;
	    font-size: 14px;	    
	}
	.showArae-items-nav div{
		position: relative;
		bottom: 10px;	
	}
	.showArae-items-nav div img{
		display: block;
		width: 160px;			
	}
	.showArae-imgs{
		float: left;
		width: 500px;
	}
	.showArae-imgs img{
		display: block;
		width: 500px;
	}
	.showArae-imgs img:nth-of-type(1){
		margin: 15px 0;
	}
	.showArae-imgs-items{
		float: left;
		width: 520px;
		padding-top: 20px;
		overflow: hidden;
	}
	.showArae-imgs-items img{
		width: 240px;
		display: block;
		float: left;
		margin-top: 15px;
		margin-left: 15px;
		_margin-left:-7.5px
	}
	img.AnimationStart{
		transition:transform 0.4s;				   
	    transform:translateX(10px);
	}
	img.AnimationEnd{
		transition:transform 0.4s;				   
	    transform:translateX(0px);
	}	
</style>