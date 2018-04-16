<style scoped>
  @import "styles/common.less";
  #app{
    margin-top: 0;
  }
</style>
<template>
  <!-- main布局组建-->
  <div class="layout">
    <Layout>
      <Header>
        <Menu mode="horizontal" theme="dark" active-name="1">
          <router-link to="/">
            <div class="layout-logo"></div>
          </router-link>
          <div class="layout-nav">
            <MenuItem name="1">
              <Icon type="ios-navigate"></Icon>
              <router-link to="/book" :style="{color:'#fff'}">图书</router-link>
            </MenuItem>
            <MenuItem name="2">
              <Icon type="ios-keypad"></Icon>
              <router-link to="/user" :style="{color:'#fff'}">用户</router-link>
            </MenuItem>
            <MenuItem name="3">
              <Icon type="ios-analytics"></Icon>
              <router-link to="/comment" :style="{color:'#fff'}">评论</router-link>
            </MenuItem>
          </div>
        </Menu>
      </Header>
      <Layout class="main-content">
        <Content :style="{minHeight: '280px'}">
          <Layout>
            <Sider class="main-siderList">
              <Menu active-name="1-2" theme="dark" width="auto">
                <Submenu name="1">
                  <template slot="title">
                    <Icon type="ios-navigate"></Icon>
                    图书
                  </template>
                  <MenuItem name="1-1"><router-link to="/book" :style="{color:'#fff'}">图书管理</router-link></MenuItem>
                </Submenu>
                <Submenu name="2">
                  <template slot="title">
                    <Icon type="ios-keypad"></Icon>
                    用户
                  </template>
                  <MenuItem name="2-1"><router-link to="/user" :style="{color:'#fff'}">用户管理</router-link></MenuItem>
                  <MenuItem name="2-2"><router-link to="/order" :style="{color:'#fff'}">订单管理</router-link></MenuItem>
                </Submenu>
                <Submenu name="3">
                  <template slot="title">
                    <Icon type="ios-analytics"></Icon>
                    评论
                  </template>
                  <MenuItem name="3-1"><router-link to="/comment" :style="{color:'#fff'}">评论管理</router-link></MenuItem>
                </Submenu>
              </Menu>
            </Sider>
          </Layout>
        </Content>
      </Layout>
      <Footer class="layout-footer-center">2013-2018 &copy; 移动书城</Footer>
    </Layout>
  </div>
  </div>
</template>
<script>
  export default {
      methods:{
        init(){
          let bigHeight = $(window).height();
          $('.main-siderList').css('height',bigHeight);
        }
      },
      mounted () {
        this.init();
     }
  }
</script>
