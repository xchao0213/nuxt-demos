<template>
    <div class="the-header">
        <div class="container">
          <nuxt-link to="/" class="logo"></nuxt-link>
          <div class="nav nav-nobar">
              <a href="/" class="nav-item active nuxt-link-active">行情</a>
              <a href="/exchange" class="nav-item">交易所</a>
              <a href="/announcement" class="nav-item">交易所公告</a>
              <a href="/media" class="nav-item">资讯</a>
              <a href="/social" class="nav-item">微博推特</a>
              <a href="/app" target="_blank" class="nav-item">App</a>
         </div>
         <div class="search-bar"><input type="search" placeholder="搜币或交易所...">
           <button class="search-btn"></button>
         </div>
         <div class="bar"></div>
         <div class="user-wrapper"><span class="login">登录</span></div>
         <div class="bar"></div>
         <a-dropdown :trigger="['click']">
            <button class="btn-dropdown btn-dropdown-lang ">
                <img class="lang" src="/flag_GBR.png" alt="">
                <span>English</span>
            </button>
            <a-menu slot="overlay" class="dropdown-lang">
            <a-menu-item key="0">
                <a href="http://www.alipay.com/"><img class="lang" src="/flag_GBR.png" alt=""><span>English</span></a>
            </a-menu-item>
            <a-menu-item key="1">
                <a href="http://www.taobao.com/"><img class="lang" src="/flag_GBR.png" alt=""><span>中文</span></a>
            </a-menu-item>            
            </a-menu>
        </a-dropdown>
        </div>
    </div>
</template>

<script>
export default {
  name: "TheHeader"
};
</script>

<style>
.the-header {
  height: 85px;
  background-color: #fff;
  -webkit-box-shadow: 0 0 18px rgba(0, 0, 0, 0.07);
  box-shadow: 0 0 18px rgba(0, 0, 0, 0.07);
  -webkit-transition: all 0.3s;
  transition: all 0.3s;
  position: fixed;
  z-index: 1;
  top: 0;
  width: 100%;
}

.container {
  display: flex;
  align-items: center;
  height: 100%;
  background-color: #fff;
  width: 1280px;
  margin: 0 auto;
}

.logo {
  width: 165px;
  height: 46px;
  display: block;
  background: url(/logo.png) no-repeat 50%/165px 46px;
}

.nav .nav-item {
  margin: 0 20px;
  color: #333;
  font-size: 14px;
  font-weight: 700;
  cursor: pointer;
}
.nav .nav-item.active {
  color: #007aff;
  position: relative;
}

.search-bar {
  margin-left: auto;
  display: flex;
  align-items: center;
}
.search-bar input {
  text-align: left;
  color: #333;
  font-size: 14px;
  font-weight: 500;
  border: 0;
  outline: 0;
  width: 120px;
  transition: all 0.3s;
  line-height: 1;
}
.search-bar .search-btn {
  background: url("/finder.png") no-repeat 50%/17px;
  height: 20px;
  width: 20px;
  cursor: pointer;
  margin-left: 10px;
}
button {
  border: 0;
  outline: 0;
  background: transparent;
}
.bar {
  background-color: #e5e5e5;
  height: 20px;
  width: 1px;
  margin: 0 20px;
}
.user-wrapper {
  display: flex;
  align-items: center;
}
.user-wrapper .login,
.user-wrapper .register {
  font-size: 14px;
  color: #333;
  font-weight: 700;
  cursor: pointer;
}
.btn-dropdown.btn-dropdown-lang {
  width: 120px;
  background: url(/icon-dropdown.svg) no-repeat 96px/8px;
}
.btn-dropdown {
  height: 34px;
  border-radius: 17px;
  border: 1px solid #e5e5e5;
  padding: 0 10px;
  display: flex;
  color: #888;
  font-size: 12px;
  align-items: center;
}

.ant-dropdown-trigger {
  cursor: pointer;
}
.lang{
    width: 20px;
    height: 20px;
    border: 1px solid #e5e5e5;
    border-radius: 50%;
}

.btn-dropdown.btn-dropdown-lang span {
    margin-left: 8px;
}
.dropdown-lang span{
    margin-left: 16px;
}
</style>

