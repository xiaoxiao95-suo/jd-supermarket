<template>
    <div id="shortCut">
       <div class="navTop">
          <ul class="nav-left">
              <li>
                <a id='aaadress'>
                    <i class="el-icon-location-outline" style="color:#e1251b"></i>
                    <span><a href="javascript:;">上海</a></span>
                </a>
                <div class="drop-down-adress" style="display:none">
                    <ul class="adress">
                        <li v-for="(item,index) in adresses1" :key="index"><a href="javascript:;">{{item}}</a></li>
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
$(function() {
    // let isShow = false
    $(".nav-left").mouseover(function() {
        $(".drop-down-adress").show()
        $(".nav-left>li").css({
            "background-color": "white",
            "border": "1px solid black"
        })

    })
    // $(".nav-left").mouseout(function() {
    //     $(".drop-down-adress").hide()
    //     $(".nav-left").css("background-color","#e3e4e5")
    // })
    $('.drop-down-adress a').click(function() {
        let $this =$(this)
        let cityName=$this.text()
        $('#aaadress span').text(cityName)
        $(".drop-down-adress").hide()

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
.nav-left {
    width: 58px;
    height: 100%;
    position: relative;
    z-index: 1000;
}
.drop-down-adress{
    width: 300px;
    background-color: white;
}
.adress {
    display: flex;
    flex-flow: wrap;
}
.drop-down-adress ul:first-child li {
    width: 20%;
}
.drop-down-adress ul:nth-child(2) li {
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