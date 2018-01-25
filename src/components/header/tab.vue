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
					{title:"智能电器",item:["电视/音响","厨房电器","居家电器","大家电","电脑数码","个人用品","热水器","取暖器"]},
					{title:"健康生活",item:["营养保健","滋补养生","儿童玩具","体育运动","生活用品","服饰","公交一卡通","定制交通卡"]},
					{title:"母婴精选",item:["婴儿奶粉","尿裤/湿巾","婴幼用品","营养辅食","妈妈用品"]},
					{title:"个人洗护",item:["面部护肤","香水、精油","男士护理","女性护理","沐浴、美发","口腔护理"]},
					{title:"饮食特产",item:["茶叶茗品","休闲零食","精品酒水","饮料、咖啡","进口食品","生鲜、水果","孔哥休闲零食","速食、特产","粮油、杂货","若谷草堂"]},
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