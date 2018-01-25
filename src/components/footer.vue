<template>
  <div class="foot">
    <div class="warper mapbg">
      <div class="foot-help">
        <ul class="clearfix">
          <li v-for="item in data">
            <h4 class="foot-title">{{item.title}}</h4>
            <p v-for="it in item.item" class="foot-text">{{it}}</p>
          </li>
        </ul>
       </div>
    </div>
    <div class="foot-prims">
      <div class="warper">
        <ul class="clearfix">
          <li><em class="li1"></em>100%正品保证</li>
          <li><em class="li2"></em>7天退换货</li>
          <li><em class="li3"></em>优质特色商品</li>
          <li><em class="li4"></em>24小时售后服务</li>
          <li><em class="li5"></em>贴心物流管家</li>
        </ul>
      </div>
    </div>
    <div class="warper">
      <div class="foot-links">
        <b>友情链接：</b>
        <a href="">合作伙伴</a>
        <a href="">联系我们</a>
        <a href="">百姓领购网</a>
        <a href="">法律声明</a>
      </div>
      <div class="copyright">
        <div class="foot-copy">
          <p><span>全国订购热线：13812503003</span><span> 电商部&nbsp;  24小时在线订购</span><span>&nbsp;</span><span>客服工作时间:</span><span>08:30--17:30</span>&nbsp;<span></span><span>Email：baixinglinggou@yeah.net</span></p>
          <p><span>&nbsp;百姓领购网</span><span>ALL Rights Reserved</span><span>&nbsp;</span><span><a href=""><span>苏ICP备15004207号-4</span></a></span></p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: [
        {
          title: "商家合作",
          item: ["促销售直通", "企业采购", "如何发货", "法律声明"]
        },
        {
          title: "售后服务",
          item: ["退换货条件", "退换货保障", "保修换货", "联系客服"]
        },
        { title: "支付方式", item: ["网银支付"] },
        { title: "配送方式", item: ["安能物流", "德邦物流", "顺丰物流"] },
        { title: "购物指南", item: ["系统指引", "联系客服", "购物流程"] }
      ]
    };
  },
  
};
</script>
<style scoped>
ul li {
  list-style: none;
}
* {
  margin: 0;
  padding: 0;
}
* {
  outline: none;
}
/* 清浮动 */
clearfix {
  zoom: 1;
}
.clearfix:after {
  content: ".";
  display: block;
  height: 0;
  clear: both;
  visibility: hidden;
}
a:hover {
  color: #bd050a;
  text-decoration: none;
}
.foot {
  background: #fff;
  margin-top: 30px;
  border-top: 1px solid #ddd;
  min-width: 1190px;
  z-index: 1;
  font-family: Microsoft yahei;
}
.warper {
  width: 1190px;
  margin: 0 auto;
  position: relative;
}
.mapbg {
  background: url(../assets/img/mapbg.png) no-repeat 85% top;
  padding: 30px 0 40px;
}
.foot-help {
  width: 1100px;
  margin-left: 75px;
}
.foot-help li {
  float: left;
  width: 170px;
  margin-left: 50px;
  color: #262626;
  padding-bottom: 5px;
}
.foot-title {
  color: #262626;
  font: 700 15px/20px microsoft yahei;
  padding-bottom: 5px;
}
.foot-text {
  font: 100 12px/24px microsoft yahei;
}
.foot-text:hover{
  color:#bd050a;
}
.foot-prims {
  background: #333;
  height: 45px;
  min-width: 1210px;
}
.foot-prims li {
  width: 20%;
  text-align: center;
  font: 16px/45px microsoft yahei;
  float: left;
  color: #fff;
}
.foot-prims li em {
  width: 40px;
  height: 30px;
  display: inline-block;
  background: url(../assets/img/foot-icn.png) no-repeat;
  position: relative;
  top: 9px;
}
.foot-prims li em.li1 {
  background-position: 0 0;
}
.foot-prims li em.li2 {
  background-position: 0 -45px;
}
.foot-prims li em.li3 {
  background-position: 0 -90px;
}
.foot-prims li em.li4 {
  background-position: 0 -135px;
}
.foot-prims li em.li5 {
  background-position: 0 -180px;
}
.foot-links {
  text-align: center;
  padding: 15px 0 0;
  font-size: 12px;
}
b {
  font-weight: normal;
}
a {
  color: #808080;
  text-decoration: none;
}
.foot-links a {
  padding: 0 5px;
  line-height: 22px;
}
.copyright {
  text-align: center;
  color: #999;
}
.foot-copy {
  font-size: 12px;
  color: #808080;
}
.foot-copy p {
  font-family: 新宋体,
    "background-color:#FFFFFF;color:#666666;text-indent:2em;text-align:center;";
}
.foot-copy p span {
  line-height: 2.5;
}
</style>

