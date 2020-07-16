<template>
    <div id="shortCut">
       <div class="navTop">
          <ul class="nav-left">
              <li>
                <a>
                    <i class="el-icon-location-outline" style="color:#e1251b"></i>
                    <span>上海</span>
                </a>
                <div class="drop-down-adress">
                    <ul>
                        <li v-for="(item,index) in adresses" :key="index">{{item}}</li>
                    </ul>
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
export default {
  name: 'NavMenu',
  data () {
    return {
        adresses: ["北京","上海","重庆","天津","河北","江苏","浙江",
        "山西","山东","安徽","河南","湖北","湖南"]
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
 .navTop ul,li {
    display: inline-block;
}
.nav-left,.nav-left li {
    width: 58px;
    height: 100%;
}
.drop-down-adress{
    position: relative;
    width: 300px;
    z-index: 1000;
}
 .nav-right li:nth-child(n+2) {
    margin-left: 10px;
    padding-left: 10px;
    border-left: 1px solid #999;
}

</style>