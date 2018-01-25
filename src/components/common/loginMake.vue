<template>
	<div id="login-make" v-show="isShowLoginMake">
		<div class="login-make-box">
			<h6><span class="login-make-close" @click="loginMakeClose">关闭</span></h6>
			<div class="login-make-box-cont">
				<div class="login-make-box-cont-title">
					<span>会员登录</span>
					<span>快速注册>></span>
				</div>
				<p class="prompt-message"><span>公共场所不建议自动登录，以防账号丢失</span></p>
				<div class="login-user">
					<label class="login-user-bg"></label>
					<input type="text" class="loginText"/>
				</div>
				<div class="login-user">
					<label class="login-password-bg"></label>
					<input type="text" class="loginText"/>
				</div>
				<div class="login-verify-box">
					<div class="login-user login-verify">
						<label class="login-verify-bg"></label>
						<input type="text" class="loginText login-verify-text"/>
					</div>
					<div class="login-verify-message">
						<span>
							<img src="../../assets/img/0.gif" alt="" />
						</span>
						<span>换张图</span>						
					</div>
				</div>
				<div class="login-setting">
					<span><input type="checkbox" /> <b>自动登录</b></span>
					<span>忘记密码</span>
				</div>
				<div  class="login-button">登录</div>
				<p class="login-prompt-message">使用合作网站账号登录:</p>
				<ul class="login-collaborates">
					<li>QQ</li>
					<li>新浪微博</li>
					<li>支付宝</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				hideLogin:false,
			}
		},
		props:["isShowLoginMake"],
		methods:{
			loginMakeClose () {		      
		      this.$emit('select-type', this.hideLogin)
		   }
		}
	}
</script>

<style>
	#login-make{
		width: 100%;
		height: 100%;
		background: rgba(0, 0, 0, 0.5);		
		z-index: 20000;
		position: absolute;
		left: 0;
		top: 0;
	}
	.login-make-box{
		width: 340px;
		margin: 0 auto;
		background: #fff;
		margin-top: 100px;
	}
	.login-make-box h6{
		line-height: 30px;
		border-bottom: 2px solid red;
		padding: 0 10px;
		overflow: hidden;
	}
	.login-make-box h6 span{
		float: right;
		font-size: 12px;
		color:#babdbf;
		font-weight:200;
	}
	.login-make-box-cont{
		padding: 0 20px;
	}
	.login-make-box-cont-title{
		margin-top: 20px;
		height: 30px;
		line-height: 30px;
	}
	.login-make-box-cont-title span:nth-child(1){
		float: left;
		font-size: 16px;
	    font-weight: bold;
	    color: #666;
	}
	.login-make-box-cont-title span:nth-child(2){
		float: right;
		color: #586dba;
		font-size: 12px;
	}
	.prompt-message{
		padding-left: 20px;			   
	    border: 1px solid #fcc079;	   
	    background: url(../../assets/img/login-icn.png) no-repeat;
	    background-position: 5px -115px;	    
	}
	.prompt-message span{
		display: block;
		background: #fffde9;
		padding: 3px 10px 3px 30px;
	    line-height: 18px;
	    height: 18px;
	    font-size: 12px;
	    color: #666;
	}
	.login-user{		
		width: 100%;
	    margin: 10px 0;	   
	    height: 34px;
	    border: 1px solid #babdbf;
	    overflow: hidden;
	}
	.login-user label{
		width: 35px;
	    height: 34px;
	    display: block;
	    float: left;
	    border-right:1px solid #babdbf ;
	}
	.loginText{
		width: 260px;	
		float: left;	
	    font: 14px/18px Microsoft yahei;
	    height: 18px;
	    padding: 8px 0;
	    border: 0;
    }
    .login-verify-box{
    	overflow: hidden;
    }
    .login-verify{
    	width: 120px;
    	float: left;
    }
    .login-verify-message{
    	float: right;
    	overflow: hidden;
    }
    .login-verify-message span{
    	display: block;    	
    }
    .login-verify-message span:nth-of-type(1){
    	float: left;
    	padding: 16px 0 0 0;
    }
    .login-verify-message span:nth-of-type(2){
    	float: right;
    	padding: 0 0 0 80px;
    	line-height: 50px;
    	font-size: 12px;
    }
    .login-verify-text{
    	width: 80px;
    }
    .login-setting{
    	overflow: hidden;
    	margin: 10px 0 20px 0;
    }
    .login-setting span:nth-of-type(1){
    	float: left;    	
    }
    .login-setting span:nth-of-type(1) input{
    	
    }
    .login-setting span:nth-of-type(1) b{
    	font-size: 12px;
    	font-weight: normal;
    	
    }
    .login-setting span:nth-of-type(2){
    	float: right;
    	font-size: 12px;
    }
    .login-button{
    	width: 100%;
    	height: 37px;
    	line-height: 37px;
    	color: #fff;
    	text-align: center;
    	background: red;
    	margin-bottom: 20px;
    }
    .login-prompt-message{
    	font-size: 12px;
    	color: #999;
    }
    .login-collaborates{
    	overflow: hidden;
    	padding: 5px 0;
    }
    .login-collaborates li{
    	color: #999;
    }
  	.login-user label{
    	background: url(../../assets/img/login-icn.png) no-repeat;
    }
    .login-make-box-cont .login-password-bg{
    	background-position: 0 -40px;
    }
    .login-make-box-cont .login-verify-bg{
    	background-position: 0 -80px;
    }
</style>