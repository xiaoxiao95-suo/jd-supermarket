<template>
    <div id="shortCut">
       <div class="navTop">
          <ul class="nav-left">
              <li>
                <a id='aaadress'>
                    <i class="el-icon-location-outline" style="color:#e1251b"></i>
                    <span>上海</span>
                </a>
                <div class="drop-down-adress">
                    <ul class="adress">
                        <li v-for="(item,index) in adresses1" :key="index">{{item}}</li>
                    </ul>
                    <div class="inner-split"></div>
                    <div class="spercial_adress">
                        <p>地区专享版本</p>
                        <ul class="adress">
                           <li v-for="(val,i) in adresses2" :key="i">{{val}}</li>
                        </ul>
                    </div>
                    ffffffff
                </div>
              </li>
          </ul>
          <ul class="nav-right">
              <li><a>你好，请登录</a> &nbsp;&nbsp;
              <a>免费注册</a></li>
              <li><a>我的订单</a></li>
              <li><a>我的京东</a></li>
              <li><a>京东会员</a></li>
              <li><a>企业采购</a></li>
              <li><a>客服服务</a></li>
              <li><a>网站导航</a></li>
              <li><a>手机京东</a></li>
          </ul>
       </div>
    </div>
</template>
<script>
$(function(){
    $('#aaadress').click(function(){
        alert('nonono')
    })
})
export default {
  name: 'NavMenu',
  data () {
    return {
        adresses1: ["北京","上海","重庆","天津","河北","江苏","浙江",
        "山西","山东","安徽","河南","湖北","湖南","新疆","四川","西藏",
        "钓鱼岛","台湾","黑龙江","辽宁","吉林","甘肃","贵州","云南","广西","广东","海外"],
        adresses2: ["中国港澳","中国台湾","京东全球"]
    }
  }
}
</script>

<style lang='scss' scoped>
#shortCut {
    background-color: #e3e4e5;
    border:1px solid #ddd;
    font-size: 12px;
}
a {
    color: #999;
}
 .navTop {
    margin: auto;
    height: 30px;
    line-height: 30px;
    width: 85%;
    display: flex;
    justify-content: space-between;
}
//  .navTop li {
//     // float: left;
//     display: inline-block;
// }
.nav-left,.nav-left>li {
    width: 58px;
    height: 100%;
}
.drop-down-adress{
    position: relative;
    width: 300px;
    z-index: 1000;
    border-left: 1px solid black;
    border-right: 1px solid black;
    border-bottom: 1px solid black;
}
.adress {
    display: flex;
    flex-flow: wrap;
}
.drop-down-adress ul:first-child li {
    // margin:0 18px 0 18px;
    width: 20%;
}
.drop-down-adress ul:nth-child(2) li {
    // margin: 0 40px 0 18px;
    // float: left;
    width: 40%;
}
.inner-split {
    margin: auto;
    width: 262px;
    height: 0;
    border-bottom: 1px dotted #eee;
}
.nav-right li {
    display: inline;
}
 .nav-right li:nth-child(n+2) {
    margin-left: 10px;
    padding-left: 10px;
    border-left: 1px solid #999;
}

</style>