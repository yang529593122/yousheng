<template>
	<div class="tab" @mouseleave="hideTab()">
			<div class="tab-title">
				<h5 v-for="item in data" @mouseover="showItem()" >{{item.title}}</h5>
			</div>			
			<div class="tab-items" v-show="dataIsShowTab">
				<div class="tab-item" v-for="item in data">
						<h6>{{item.title}}</h6>
						<div>
							<span v-for="it in item.item">{{it}}</span>
						</div>
				</div>
			</div>
	</div>
</template>

<script>
	export default{
		data(){
			return {
				data:[
					{title:"智能电器",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"健康生活",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"母婴精选",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"个人洗护",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"饮食特产",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"员工福利",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"企业专属",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]},
					{title:"公益活动",item:["sdfsdf","sdfsdf","sdfsdf","sdfsdf","sdfsdf"]}
				],
				dataIsShowTab:false,
			}
			
		},
		/*props:["dataIsShowTab"],*/
		methods:{
			showItem(){				
				this.dataIsShowTab=true
			},
			hideTab(){
				this.dataIsShowTab=false
			}
		}
	}
</script>

<style>
	.tab{
		overflow: hidden;
		position: absolute;
		top:40px;
		z-index: 10000;
	}
	.tab-title{
		float: left;
		width: 210px;
	}
	.tab-title h5{
		text-decoration: none;				
		font-size: 18px;       
        font-weight: 400;
    	letter-spacing: 5px;
    	line-height: 52px;
    	border-bottom: 1px dashed #fff;
    	background: red;
    	color: #fff;
	}
	
	.tab-items{
		float: left;
		background: #fff;
		width: 700px;
		height: 424px;
		padding:0 35px;
		border: 1px solid #ccc;
	}
	.tab-items h6{
		color: red;
	}
	.tab-item{
		border-bottom: 1px dashed #ccc;
		padding: 5px 0;
	}
	.tab div{
		overflow: hidden;
	}
	.tab-item span{
		float: left;
		padding: 0 5px;
		display: block;
	}
</style>