<template>
	<div class="Life">
		<div>
			<img src="../assets/weinituijian.png" alt="" />
		</div>
		<div class="imgs-box">
			<div class="imgs-box-left">
				<img src="../assets/201709200346328.jpg" alt="" />
			</div>
			<div class="imgs-box-cont">
				<div class="imgs-box-item">
					<img src="../assets/img/10.jpg" alt="" />
				</div>
				<div class="imgs-box-item">
					<img src="../assets/img/10.jpg" alt="" />
				</div>
				<div class="imgs-box-item">
					<img src="../assets/img/10.jpg" alt="" />
				</div>
				<div class="imgs-box-item">
					<img src="../assets/img/10.jpg" alt="" />
				</div>
			</div>
			<div class="imgs-box-right">
				<img src="../assets/201709200346328.jpg" alt="" />
			</div>
		</div>
		<div class="imgs-life-bottom">
			<img src="../assets/weinituijian.png" alt="" />
		</div>
	</div>
</template>

<script>
	require ("../assets/weinituijian.png")
	require ("../assets/201709200346328.jpg")
</script>

<style>
	.Life{
		width:1190px;
		margin: 20px auto;
		overflow: hidden;
	}
	.Life img{
		display: block;
	}
	.imgs-box-left{
		float: left;
		margin-right: 25px;
	}
	.imgs-box-cont{
		float: left;
		width: 600px;
		overflow: hidden;
		
	}
	.imgs-box-right{
		float: right;
	}
	.imgs-box-item{
		float: left;
	}
	.imgs-life-bottom{
		clear: both;
		margin: 20px 0;
	}
</style>