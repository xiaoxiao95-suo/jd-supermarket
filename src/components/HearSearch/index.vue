<template>
    <div>
      <div class="w">
        <div class="searchForm">
          <div class="searchBox">
              <input type="text">
              <span>
                <i class="el-icon-camera"></i>
              </span> 
              <button>
                  <i class="el-icon-search" style="color:white;"></i>
              </button>
          </div>
          <div class="shopCard">
            <span>
              <i class="el-icon-shopping-cart-2" style="color:#e2231a; font-weight:bold"></i>
              <a href="">我的购物车</a>
            </span>
          </div>
        </div>
        <div class="navSettle">
          <div class="navItems">
            <ul id="navgroups1">
              <li v-for="(item,index) in navItems.nav1Items" :key="index"><a href="#">{{item}}</a></li>
            </ul>
            <ul id="navgroups2">
              <li v-for="(item,index) in navItems.nav2Items" :key="index"><a href="#">{{item}}</a></li>
            </ul>
            <ul id="navgroups3">
              <li v-for="(item,index) in navItems.nav3Items" :key="index"><a href="#">{{item}}</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  name: 'HeaderSearch',
  data () {
    return {
      navItems: {
        nav1Items: ["秒杀","优惠券","PLUS会员","品牌闪购"],
        nav2Items: ["拍卖","京东家电","京东超市","京东生鲜"],
        nav3Items: ["京东国际","京东金融"]
      }
      
    }
  }
}
</script>

<style lang='scss' scoped>
.w {
  height: 140px;
  position: relative;
  border: 1px solid #ddd;
}
.searchForm {
  padding-top: 25px;
  margin: auto;
  display: flex;
  justify-content: center;
}
.searchBox {
  border: 2px solid #e2231a;
}
.searchBox input {
    height: 26px;
    width: 400px;
    outline: none;
    padding:2px 44px 2px 17px;
    border:1px solid transparent;
}
.searchBox button {
    width:56px;
    height: 32px;
    background-color: #e2231a;
    border:none;
    margin-left: 20px;
}
.shopCard {
  margin-left: 20px;
  border: 1px solid #e3e4e5;
  padding: 0 13px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.shopCard i {
  margin-right: 13px;
}
.shopCard a {
  text-decoration: none;
  color: #e2231a;
  font-size: 12px;
}
.navSettle {
  position: absolute;
  bottom: 10px;
  width: 100%;
}
.navItems ul {
  display: inline;
}
.navItems li{
  display: inline;
  margin-right: 20px;
}
#navgroups1 li:nth-child(-n+2) a {
  font-weight: bold;
  color: #e1251b;
}
</style>